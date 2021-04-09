---
title: ScheduleByDay (calendarTriggerType) 元素
description: 指定每日排程。
ms.assetid: 5a6097ce-a855-4b08-84c5-71f06343805e
keywords:
- XML 元素工作排程器每日觸發程式
- ScheduleByDay 元素工作排程器
topic_type:
- apiref
api_name:
- ScheduleByDay
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 614777ede63605dc7ed6936bda952c6071bda371
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934866"
---
# <a name="schedulebyday-calendartriggertype-element"></a><span data-ttu-id="72454-105">ScheduleByDay (calendarTriggerType) 元素</span><span class="sxs-lookup"><span data-stu-id="72454-105">ScheduleByDay (calendarTriggerType) Element</span></span>

<span data-ttu-id="72454-106">指定每日排程。</span><span class="sxs-lookup"><span data-stu-id="72454-106">Specifies a daily schedule.</span></span> <span data-ttu-id="72454-107">例如，工作會在每天上午8:00、每天、每隔三天開始，依此類推。</span><span class="sxs-lookup"><span data-stu-id="72454-107">For example, the task starts at 8:00 AM every day, every-other day, every third day, and so on.</span></span>

``` syntax
<xs:element name="ScheduleByDay"
    type="dailyScheduleType"
 />
```

<span data-ttu-id="72454-108">**ScheduleByDay** 元素是由 [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="72454-108">The **ScheduleByDay** element is defined by the [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="72454-109">父元素</span><span class="sxs-lookup"><span data-stu-id="72454-109">Parent element</span></span>



| <span data-ttu-id="72454-110">元素</span><span class="sxs-lookup"><span data-stu-id="72454-110">Element</span></span>                                                                             | <span data-ttu-id="72454-111">衍生自</span><span class="sxs-lookup"><span data-stu-id="72454-111">Derived from</span></span>                                                                       | <span data-ttu-id="72454-112">Description</span><span class="sxs-lookup"><span data-stu-id="72454-112">Description</span></span>                                                                                |
|-------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="72454-113">**CalendarTrigger**</span><span class="sxs-lookup"><span data-stu-id="72454-113">**CalendarTrigger**</span></span>](taskschedulerschema-calendartrigger-triggergroup-element.md) | [<span data-ttu-id="72454-114">**calendarTriggerType**</span><span class="sxs-lookup"><span data-stu-id="72454-114">**calendarTriggerType**</span></span>](taskschedulerschema-calendartriggertype-complextype.md) | <span data-ttu-id="72454-115">指定每日、每週、每月或每週 (DOW) 觸發程式。</span><span class="sxs-lookup"><span data-stu-id="72454-115">Specifies a daily, weekly, monthly, or a monthly day-of-the-week (DOW) trigger.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="72454-116">子元素</span><span class="sxs-lookup"><span data-stu-id="72454-116">Child elements</span></span>



| <span data-ttu-id="72454-117">元素</span><span class="sxs-lookup"><span data-stu-id="72454-117">Element</span></span>                                                                            | <span data-ttu-id="72454-118">類型</span><span class="sxs-lookup"><span data-stu-id="72454-118">Type</span></span>             | <span data-ttu-id="72454-119">Description</span><span class="sxs-lookup"><span data-stu-id="72454-119">Description</span></span>                                                         |
|------------------------------------------------------------------------------------|------------------|---------------------------------------------------------------------|
| [<span data-ttu-id="72454-120">**DaysInterval**</span><span class="sxs-lookup"><span data-stu-id="72454-120">**DaysInterval**</span></span>](taskschedulerschema-daysinterval-dailyscheduletype-element.md) | <span data-ttu-id="72454-121">**unsignedByte**</span><span class="sxs-lookup"><span data-stu-id="72454-121">**unsignedByte**</span></span> | <span data-ttu-id="72454-122">指定排程中天數之間的間隔。</span><span class="sxs-lookup"><span data-stu-id="72454-122">Specifies the interval between the days in the schedule.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="72454-123">備註</span><span class="sxs-lookup"><span data-stu-id="72454-123">Remarks</span></span>

<span data-ttu-id="72454-124">先前所列的子項目是由 [**dailyScheduleType**](taskschedulerschema-dailyscheduletype-complextype.md) 複雜元素類型所定義。</span><span class="sxs-lookup"><span data-stu-id="72454-124">The child element listed previously is defined by the [**dailyScheduleType**](taskschedulerschema-dailyscheduletype-complextype.md) complex element types.</span></span>

<span data-ttu-id="72454-125">工作開始的當日時間是由 [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) 元素設定。</span><span class="sxs-lookup"><span data-stu-id="72454-125">The time of day that the task is started is set by the [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) element.</span></span>

<span data-ttu-id="72454-126">針對開發腳本，會使用 [**DailyTrigger**](weeklytrigger.md) 物件指定每日觸發程式。</span><span class="sxs-lookup"><span data-stu-id="72454-126">For scripting development, a daily trigger is specified using the [**DailyTrigger**](weeklytrigger.md) object.</span></span>

<span data-ttu-id="72454-127">針對 c + + 開發，會使用 [**IDailyTrigger**](/windows/desktop/api/taskschd/nn-taskschd-idailytrigger) 介面指定每日觸發程式。</span><span class="sxs-lookup"><span data-stu-id="72454-127">For C++ development, a daily trigger is specified using the [**IDailyTrigger**](/windows/desktop/api/taskschd/nn-taskschd-idailytrigger) interface.</span></span>

## <a name="examples"></a><span data-ttu-id="72454-128">範例</span><span class="sxs-lookup"><span data-stu-id="72454-128">Examples</span></span>

<span data-ttu-id="72454-129">下列 XML 會定義每日啟動工作的每日行事曆觸發程式。</span><span class="sxs-lookup"><span data-stu-id="72454-129">The following XML defines a daily calendar trigger that starts the task every day.</span></span>


```XML
<CalendarTrigger>
    <StartBoundary>2005-01-01T00:00:00</StartBoundary>
    <EndBounadry>2007-01-01T00:00:00</EndBoundary>
    <ScheduleByDay>
        <DaysInterval>1</DaysInterval>
    </ScheduleByDay>
</CalendarTrigger>
```



<span data-ttu-id="72454-130">如需指定每日排程之工作的 XML 完整範例，請參閱 [ (XML) 的每日觸發程式範例 ](daily-trigger-example--xml-.md)。</span><span class="sxs-lookup"><span data-stu-id="72454-130">For a complete example of the XML for a task that specifies a daily schedule, see [Daily Trigger Example (XML)](daily-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="72454-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="72454-131">Requirements</span></span>



| <span data-ttu-id="72454-132">需求</span><span class="sxs-lookup"><span data-stu-id="72454-132">Requirement</span></span> | <span data-ttu-id="72454-133">值</span><span class="sxs-lookup"><span data-stu-id="72454-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="72454-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="72454-134">Minimum supported client</span></span><br/> | <span data-ttu-id="72454-135">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="72454-135">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="72454-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="72454-136">Minimum supported server</span></span><br/> | <span data-ttu-id="72454-137">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="72454-137">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="72454-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="72454-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72454-139">工作排程器架構元素</span><span class="sxs-lookup"><span data-stu-id="72454-139">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="72454-140">工作排程器</span><span class="sxs-lookup"><span data-stu-id="72454-140">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





