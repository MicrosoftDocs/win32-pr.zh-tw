---
title: ScheduleByMonth (calendarTriggerType) 元素
description: 指定每月排程。
ms.assetid: 3a23f4d0-bdaf-4f2a-81c6-8652a0849fc8
keywords:
- ScheduleByMonth 元素工作排程器
topic_type:
- apiref
api_name:
- ScheduleByMonth
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6fda84a1cd4373f7988fa66a5ad70c97dd371d4d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105360"
---
# <a name="schedulebymonth-calendartriggertype-element"></a><span data-ttu-id="64e6e-104">ScheduleByMonth (calendarTriggerType) 元素</span><span class="sxs-lookup"><span data-stu-id="64e6e-104">ScheduleByMonth (calendarTriggerType) Element</span></span>

<span data-ttu-id="64e6e-105">指定每月排程。</span><span class="sxs-lookup"><span data-stu-id="64e6e-105">Specifies a monthly schedule.</span></span> <span data-ttu-id="64e6e-106">例如，工作會在每月特定日子的特定月份從上午8:00 開始。</span><span class="sxs-lookup"><span data-stu-id="64e6e-106">For example, the task starts at 8:00 AM on specific days of the month on specific months.</span></span>

``` syntax
<xs:element name="ScheduleByMonth"
    type="monthlyScheduleType"
 />
```

<span data-ttu-id="64e6e-107">**ScheduleByMonth** 元素是由 [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="64e6e-107">The **ScheduleByMonth** element is defined by the [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="64e6e-108">父元素</span><span class="sxs-lookup"><span data-stu-id="64e6e-108">Parent element</span></span>



| <span data-ttu-id="64e6e-109">元素</span><span class="sxs-lookup"><span data-stu-id="64e6e-109">Element</span></span>                                                                             | <span data-ttu-id="64e6e-110">衍生自</span><span class="sxs-lookup"><span data-stu-id="64e6e-110">Derived from</span></span>                                                                       | <span data-ttu-id="64e6e-111">Description</span><span class="sxs-lookup"><span data-stu-id="64e6e-111">Description</span></span>                                                                                |
|-------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="64e6e-112">**CalendarTrigger**</span><span class="sxs-lookup"><span data-stu-id="64e6e-112">**CalendarTrigger**</span></span>](taskschedulerschema-calendartrigger-triggergroup-element.md) | [<span data-ttu-id="64e6e-113">**calendarTriggerType**</span><span class="sxs-lookup"><span data-stu-id="64e6e-113">**calendarTriggerType**</span></span>](taskschedulerschema-calendartriggertype-complextype.md) | <span data-ttu-id="64e6e-114">指定每日、每週、每月或每週 (DOW) 觸發程式。</span><span class="sxs-lookup"><span data-stu-id="64e6e-114">Specifies a daily, weekly, monthly, or a monthly day-of-the-week (DOW) trigger.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="64e6e-115">子元素</span><span class="sxs-lookup"><span data-stu-id="64e6e-115">Child elements</span></span>



| <span data-ttu-id="64e6e-116">元素</span><span class="sxs-lookup"><span data-stu-id="64e6e-116">Element</span></span>                                                                                                  | <span data-ttu-id="64e6e-117">類型</span><span class="sxs-lookup"><span data-stu-id="64e6e-117">Type</span></span>                                                                       | <span data-ttu-id="64e6e-118">Description</span><span class="sxs-lookup"><span data-stu-id="64e6e-118">Description</span></span>                                                             |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [<span data-ttu-id="64e6e-119">**DaysOfMonth (monthlyScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="64e6e-119">**DaysOfMonth (monthlyScheduleType)**</span></span>](taskschedulerschema-daysofmonth-monthlyscheduletype-element.md) | [<span data-ttu-id="64e6e-120">**daysOfMonthType**</span><span class="sxs-lookup"><span data-stu-id="64e6e-120">**daysOfMonthType**</span></span>](taskschedulerschema-daysofmonthtype-complextype.md) | <span data-ttu-id="64e6e-121">指定工作執行的當月天數。</span><span class="sxs-lookup"><span data-stu-id="64e6e-121">Specifies the days of the month during which the task runs.</span></span><br/>  |
| [<span data-ttu-id="64e6e-122">**MonthlyScheduleType) 的月份 (**</span><span class="sxs-lookup"><span data-stu-id="64e6e-122">**Months (monthlyScheduleType)**</span></span>](taskschedulerschema-months-monthlyscheduletype-element.md)           | [<span data-ttu-id="64e6e-123">**monthsType**</span><span class="sxs-lookup"><span data-stu-id="64e6e-123">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md)           | <span data-ttu-id="64e6e-124">指定執行工作的年份月份。</span><span class="sxs-lookup"><span data-stu-id="64e6e-124">Specifies the months of the year during which the task runs.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="64e6e-125">備註</span><span class="sxs-lookup"><span data-stu-id="64e6e-125">Remarks</span></span>

<span data-ttu-id="64e6e-126">工作開始的當日時間是由 [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) 元素設定。</span><span class="sxs-lookup"><span data-stu-id="64e6e-126">The time of day that the task is started is set by the [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) element.</span></span>

<span data-ttu-id="64e6e-127">針對腳本開發，會使用 [**MonthlyTrigger**](monthlytrigger.md) 物件指定每月觸發程式。</span><span class="sxs-lookup"><span data-stu-id="64e6e-127">For script development, a monthly trigger is specified using the [**MonthlyTrigger**](monthlytrigger.md) object.</span></span>

<span data-ttu-id="64e6e-128">針對 c + + 開發，每月觸發程式都是使用 [**IMonthlyTrigger**](/windows/desktop/api/taskschd/nn-taskschd-imonthlytrigger) 介面指定。</span><span class="sxs-lookup"><span data-stu-id="64e6e-128">For C++ development, a monthly trigger is specified using the [**IMonthlyTrigger**](/windows/desktop/api/taskschd/nn-taskschd-imonthlytrigger) interface.</span></span>

<span data-ttu-id="64e6e-129">下列子專案是由 [**monthlyScheduleType**](taskschedulerschema-monthlyscheduletype-complextype.md) 複雜元素類型所定義。</span><span class="sxs-lookup"><span data-stu-id="64e6e-129">The child elements listed below are defined by the [**monthlyScheduleType**](taskschedulerschema-monthlyscheduletype-complextype.md) complex element types.</span></span>

## <a name="examples"></a><span data-ttu-id="64e6e-130">範例</span><span class="sxs-lookup"><span data-stu-id="64e6e-130">Examples</span></span>

<span data-ttu-id="64e6e-131">下列 XML 會定義每月的行事曆觸發程式，此觸發程式會在每個月的第1天和第15天開始 ( 于上午8:00 點) 。</span><span class="sxs-lookup"><span data-stu-id="64e6e-131">The following XML defines a monthly calendar trigger that starts a task ( at 8:00 AM) on the 1st and 15th day of every month of the year.</span></span>


```XML
<CalendarTrigger>
    <StartBoundary>2005-01-01T08:00:00</StartBoundary>
    <EndBounadry>2007-01-01T00:00:00</EndBoundary>
    <ScheduleByMonth>
        <DaysOfMonth>
            <Day>1</Day>
            <Day>15</Day>
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
        </Months>
    </ScheduleByMonth>
</CalendarTrigger>
```



## <a name="requirements"></a><span data-ttu-id="64e6e-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="64e6e-132">Requirements</span></span>



| <span data-ttu-id="64e6e-133">需求</span><span class="sxs-lookup"><span data-stu-id="64e6e-133">Requirement</span></span> | <span data-ttu-id="64e6e-134">值</span><span class="sxs-lookup"><span data-stu-id="64e6e-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="64e6e-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="64e6e-135">Minimum supported client</span></span><br/> | <span data-ttu-id="64e6e-136">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="64e6e-136">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="64e6e-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="64e6e-137">Minimum supported server</span></span><br/> | <span data-ttu-id="64e6e-138">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="64e6e-138">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="64e6e-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="64e6e-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64e6e-140">工作排程器架構元素</span><span class="sxs-lookup"><span data-stu-id="64e6e-140">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="64e6e-141">工作排程器</span><span class="sxs-lookup"><span data-stu-id="64e6e-141">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





