---
title: MonthlyDayOfWeekScheduleType) 元素 (月份
description: 指定在一年中的幾個月，工作會在一年中執行一周的每月日排程。
ms.assetid: 420fa7f4-7106-483e-9b3b-d1ba51f25222
keywords:
- Months 元素工作排程器
topic_type:
- apiref
api_name:
- Months
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 76f13a5823e0154519dbdb093dd03ea36bbe77b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384222"
---
# <a name="months-monthlydayofweekscheduletype-element"></a><span data-ttu-id="921d6-104">MonthlyDayOfWeekScheduleType) 元素 (月份</span><span class="sxs-lookup"><span data-stu-id="921d6-104">Months (monthlyDayOfWeekScheduleType) Element</span></span>

<span data-ttu-id="921d6-105">指定在一年中的幾個月，工作會在一年中執行一周的每月日排程。</span><span class="sxs-lookup"><span data-stu-id="921d6-105">Specifies the months of the year during which the task runs for a monthly day-of-week schedule.</span></span>

``` syntax
<xs:element name="Months"
    type="monthsType"
 />
```

<span data-ttu-id="921d6-106">**Months** 元素是由 [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="921d6-106">The **Months** element is defined by the [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="921d6-107">父元素</span><span class="sxs-lookup"><span data-stu-id="921d6-107">Parent element</span></span>



| <span data-ttu-id="921d6-108">元素</span><span class="sxs-lookup"><span data-stu-id="921d6-108">Element</span></span>                                                                                                                            | <span data-ttu-id="921d6-109">衍生自</span><span class="sxs-lookup"><span data-stu-id="921d6-109">Derived from</span></span>                                                                                         | <span data-ttu-id="921d6-110">Description</span><span class="sxs-lookup"><span data-stu-id="921d6-110">Description</span></span>                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="921d6-111">**ScheduleByMonthDayOfWeek (calendarTriggerType)**</span><span class="sxs-lookup"><span data-stu-id="921d6-111">**ScheduleByMonthDayOfWeek (calendarTriggerType)**</span></span>](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) | [<span data-ttu-id="921d6-112">**monthlyDayOfWeekScheduleType**</span><span class="sxs-lookup"><span data-stu-id="921d6-112">**monthlyDayOfWeekScheduleType**</span></span>](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) | <span data-ttu-id="921d6-113">指定啟動工作的觸發程式，此觸發程式會每個月的每週工作日排程。</span><span class="sxs-lookup"><span data-stu-id="921d6-113">Specifies a trigger that starts a job for a monthly day-of-week schedule.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="921d6-114">子元素</span><span class="sxs-lookup"><span data-stu-id="921d6-114">Child elements</span></span>



| <span data-ttu-id="921d6-115">元素</span><span class="sxs-lookup"><span data-stu-id="921d6-115">Element</span></span>                                                               | <span data-ttu-id="921d6-116">類型</span><span class="sxs-lookup"><span data-stu-id="921d6-116">Type</span></span> | <span data-ttu-id="921d6-117">Description</span><span class="sxs-lookup"><span data-stu-id="921d6-117">Description</span></span>                                           |
|-----------------------------------------------------------------------|------|-------------------------------------------------------|
| [<span data-ttu-id="921d6-118">**4 月**</span><span class="sxs-lookup"><span data-stu-id="921d6-118">**April**</span></span>](taskschedulerschema-april-monthstype-element.md)         |      | <span data-ttu-id="921d6-119">指定工作會在四月執行。</span><span class="sxs-lookup"><span data-stu-id="921d6-119">Specifies that the task runs in April.</span></span><br/>     |
| [<span data-ttu-id="921d6-120">**8 月**</span><span class="sxs-lookup"><span data-stu-id="921d6-120">**August**</span></span>](taskschedulerschema-august-monthstype-element.md)       |      | <span data-ttu-id="921d6-121">指定工作在8月執行。</span><span class="sxs-lookup"><span data-stu-id="921d6-121">Specifies that the task runs in August.</span></span><br/>    |
| [<span data-ttu-id="921d6-122">**12 月**</span><span class="sxs-lookup"><span data-stu-id="921d6-122">**December**</span></span>](taskschedulerschema-december-monthstype-element.md)   |      | <span data-ttu-id="921d6-123">指定工作會在十二月執行。</span><span class="sxs-lookup"><span data-stu-id="921d6-123">Specifies that the task runs in December.</span></span><br/>  |
| [<span data-ttu-id="921d6-124">**2 月**</span><span class="sxs-lookup"><span data-stu-id="921d6-124">**February**</span></span>](taskschedulerschema-february-monthstype-element.md)   |      | <span data-ttu-id="921d6-125">指定工作會在二月執行。</span><span class="sxs-lookup"><span data-stu-id="921d6-125">Specifies that the task runs in February.</span></span><br/>  |
| [<span data-ttu-id="921d6-126">**1 月**</span><span class="sxs-lookup"><span data-stu-id="921d6-126">**January**</span></span>](taskschedulerschema-january-monthstype-element.md)     |      | <span data-ttu-id="921d6-127">指定工作會在一月執行。</span><span class="sxs-lookup"><span data-stu-id="921d6-127">Specifies that the task runs in January.</span></span><br/>   |
| [<span data-ttu-id="921d6-128">**7 月**</span><span class="sxs-lookup"><span data-stu-id="921d6-128">**July**</span></span>](taskschedulerschema-july-monthstype-element.md)           |      | <span data-ttu-id="921d6-129">指定工作會在七月執行。</span><span class="sxs-lookup"><span data-stu-id="921d6-129">Specifies that the task runs in July.</span></span><br/>      |
| [<span data-ttu-id="921d6-130">**6 月**</span><span class="sxs-lookup"><span data-stu-id="921d6-130">**June**</span></span>](taskschedulerschema-june-monthstype-element.md)           |      | <span data-ttu-id="921d6-131">指定工作在六月執行。</span><span class="sxs-lookup"><span data-stu-id="921d6-131">Specifies that the task runs in June.</span></span><br/>      |
| [<span data-ttu-id="921d6-132">**3 月**</span><span class="sxs-lookup"><span data-stu-id="921d6-132">**March**</span></span>](taskschedulerschema-march-monthstype-element.md)         |      | <span data-ttu-id="921d6-133">指定工作在三月執行。</span><span class="sxs-lookup"><span data-stu-id="921d6-133">Specifies that the task runs in March.</span></span><br/>     |
| [<span data-ttu-id="921d6-134">**五月**</span><span class="sxs-lookup"><span data-stu-id="921d6-134">**May**</span></span>](taskschedulerschema-may-monthstype-element.md)             |      | <span data-ttu-id="921d6-135">指定工作在5月執行。</span><span class="sxs-lookup"><span data-stu-id="921d6-135">Specifies that the task runs in May.</span></span><br/>       |
| [<span data-ttu-id="921d6-136">**11 月**</span><span class="sxs-lookup"><span data-stu-id="921d6-136">**November**</span></span>](taskschedulerschema-november-monthstype-element.md)   |      | <span data-ttu-id="921d6-137">指定工作在11月執行。</span><span class="sxs-lookup"><span data-stu-id="921d6-137">Specifies that the task runs in November.</span></span><br/>  |
| [<span data-ttu-id="921d6-138">**10 月**</span><span class="sxs-lookup"><span data-stu-id="921d6-138">**October**</span></span>](taskschedulerschema-october-monthstype-element.md)     |      | <span data-ttu-id="921d6-139">指定工作在十月執行。</span><span class="sxs-lookup"><span data-stu-id="921d6-139">Specifies that the task runs in October.</span></span><br/>   |
| [<span data-ttu-id="921d6-140">**9 月**</span><span class="sxs-lookup"><span data-stu-id="921d6-140">**September**</span></span>](taskschedulerschema-september-monthstype-element.md) |      | <span data-ttu-id="921d6-141">指定工作在九月執行。</span><span class="sxs-lookup"><span data-stu-id="921d6-141">Specifies that the task runs in September.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="921d6-142">備註</span><span class="sxs-lookup"><span data-stu-id="921d6-142">Remarks</span></span>

<span data-ttu-id="921d6-143">在撰寫腳本時，會使用 [**MonthlyDOWTrigger. MonthsOfYear**](monthlydowtrigger-monthsofyear.md) 屬性指定一年中每月星期幾的月份。</span><span class="sxs-lookup"><span data-stu-id="921d6-143">For scripting development, the months of a year for a monthly day-of-week schedule are specified using the [**MonthlyDOWTrigger.MonthsOfYear**](monthlydowtrigger-monthsofyear.md) property.</span></span>

<span data-ttu-id="921d6-144">若是 c + + 開發，則會使用 [**IMonthlyDOWTrigger：： MonthsOfYear**](/windows/desktop/api/taskschd/nf-taskschd-imonthlydowtrigger-get_monthsofyear) 屬性指定一年中每月星期幾的月份。</span><span class="sxs-lookup"><span data-stu-id="921d6-144">For C++ development, the months of a year for a monthly day-of-week schedule are specified using the [**IMonthlyDOWTrigger::MonthsOfYear**](/windows/desktop/api/taskschd/nf-taskschd-imonthlydowtrigger-get_monthsofyear) property.</span></span>

<span data-ttu-id="921d6-145">上述的子項目是由 [**monthsType**](taskschedulerschema-monthstype-complextype.md) 複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="921d6-145">The child elements above are defined by the [**monthsType**](taskschedulerschema-monthstype-complextype.md) complex type.</span></span>

## <a name="examples"></a><span data-ttu-id="921d6-146">範例</span><span class="sxs-lookup"><span data-stu-id="921d6-146">Examples</span></span>

<span data-ttu-id="921d6-147">下列 XML 會定義每月的每週工作日行事曆，此日曆會在每個月的第一周的星期一開始工作。</span><span class="sxs-lookup"><span data-stu-id="921d6-147">The following XML defines a monthly day-of-week calendar that starts the task on Monday of the first week for each month of the year.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="921d6-148">規格需求</span><span class="sxs-lookup"><span data-stu-id="921d6-148">Requirements</span></span>



| <span data-ttu-id="921d6-149">需求</span><span class="sxs-lookup"><span data-stu-id="921d6-149">Requirement</span></span> | <span data-ttu-id="921d6-150">值</span><span class="sxs-lookup"><span data-stu-id="921d6-150">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="921d6-151">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="921d6-151">Minimum supported client</span></span><br/> | <span data-ttu-id="921d6-152">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="921d6-152">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="921d6-153">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="921d6-153">Minimum supported server</span></span><br/> | <span data-ttu-id="921d6-154">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="921d6-154">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="921d6-155">另請參閱</span><span class="sxs-lookup"><span data-stu-id="921d6-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="921d6-156">工作排程器架構元素</span><span class="sxs-lookup"><span data-stu-id="921d6-156">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="921d6-157">工作排程器</span><span class="sxs-lookup"><span data-stu-id="921d6-157">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





