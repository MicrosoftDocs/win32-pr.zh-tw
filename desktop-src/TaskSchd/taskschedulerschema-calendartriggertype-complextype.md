---
title: calendarTriggerType 複雜類型
description: 定義月曆元素的子項目和排序資訊。
ms.assetid: bf0d964e-aff2-4807-b086-c504f8963663
keywords:
- calendarTriggerType 複雜類型工作排程器
topic_type:
- apiref
api_name:
- calendarTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6f45434fa68b6300157a29318ba257f43bac5992
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106976359"
---
# <a name="calendartriggertype-complex-type"></a><span data-ttu-id="8623c-104">calendarTriggerType 複雜類型</span><span class="sxs-lookup"><span data-stu-id="8623c-104">calendarTriggerType Complex Type</span></span>

<span data-ttu-id="8623c-105">定義月曆元素的子項目和排序資訊。</span><span class="sxs-lookup"><span data-stu-id="8623c-105">Defines the child elements and sequencing information for calendar elements.</span></span>

``` syntax
<xs:complexType name="calendarTriggerType">
    <xs:complexContent>
        <xs:extension
            base="triggerBaseType"
        >
            <xs:sequence>
                <xs:element name="RandomDelay"
                    type="duration"
                    default="PT0M"
                    minOccurs="0"
                 />
                <xs:choice>
                    <xs:element name="ScheduleByDay"
                        type="dailyScheduleType"
                     />
                    <xs:element name="ScheduleByWeek"
                        type="weeklyScheduleType"
                     />
                    <xs:element name="ScheduleByMonth"
                        type="monthlyScheduleType"
                     />
                    <xs:element name="ScheduleByMonthDayOfWeek"
                        type="monthlyDayOfWeekScheduleType"
                     />
                </xs:choice>
            </xs:sequence>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="8623c-106">子元素</span><span class="sxs-lookup"><span data-stu-id="8623c-106">Child elements</span></span>



| <span data-ttu-id="8623c-107">元素</span><span class="sxs-lookup"><span data-stu-id="8623c-107">Element</span></span>                                                                                                      | <span data-ttu-id="8623c-108">類型</span><span class="sxs-lookup"><span data-stu-id="8623c-108">Type</span></span>                                                                                                 | <span data-ttu-id="8623c-109">Description</span><span class="sxs-lookup"><span data-stu-id="8623c-109">Description</span></span>                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8623c-110">**RandomDelay**</span><span class="sxs-lookup"><span data-stu-id="8623c-110">**RandomDelay**</span></span>](taskschedulerschema-randomdelay-calendartriggertype-element.md)                           | <span data-ttu-id="8623c-111">duration</span><span class="sxs-lookup"><span data-stu-id="8623c-111">duration</span></span>                                                                                             | <span data-ttu-id="8623c-112">包含隨機新增至觸發程式開始時間的延遲時間。</span><span class="sxs-lookup"><span data-stu-id="8623c-112">Contains the delay time that is randomly added to the start time of the trigger.</span></span> <span data-ttu-id="8623c-113">此字串的格式為 P <days> DT <hours> H <minutes> M <seconds> S (例如，P2DT5S 是2天、5秒的延遲) 。</span><span class="sxs-lookup"><span data-stu-id="8623c-113">The format for this string is P<days>DT<hours>H<minutes>M<seconds>S (for example, P2DT5S is a 2 day, 5 second delay).</span></span><br/> |
| [<span data-ttu-id="8623c-114">**ScheduleByDay**</span><span class="sxs-lookup"><span data-stu-id="8623c-114">**ScheduleByDay**</span></span>](taskschedulerschema-schedulebyday-calendartriggertype-element.md)                       | [<span data-ttu-id="8623c-115">**dailyScheduleType**</span><span class="sxs-lookup"><span data-stu-id="8623c-115">**dailyScheduleType**</span></span>](taskschedulerschema-dailyscheduletype-complextype.md)                       | <span data-ttu-id="8623c-116">指定每日排程。</span><span class="sxs-lookup"><span data-stu-id="8623c-116">Specifies a daily schedule.</span></span> <span data-ttu-id="8623c-117">例如，工作會在每天、每隔三天、每隔三天開始，依此類推。</span><span class="sxs-lookup"><span data-stu-id="8623c-117">For example, the task starts every day, every-other day, every third day, and so on.</span></span><br/>                                                                                                               |
| [<span data-ttu-id="8623c-118">**ScheduleByMonth**</span><span class="sxs-lookup"><span data-stu-id="8623c-118">**ScheduleByMonth**</span></span>](taskschedulerschema-schedulebymonth-calendartriggertype-element.md)                   | [<span data-ttu-id="8623c-119">**monthlyScheduleType**</span><span class="sxs-lookup"><span data-stu-id="8623c-119">**monthlyScheduleType**</span></span>](taskschedulerschema-monthlyscheduletype-complextype.md)                   | <span data-ttu-id="8623c-120">指定每月排程。</span><span class="sxs-lookup"><span data-stu-id="8623c-120">Specifies a monthly schedule.</span></span> <span data-ttu-id="8623c-121">例如，工作會在每月特定日子的特定月份從上午8:00 開始。</span><span class="sxs-lookup"><span data-stu-id="8623c-121">For example, the task starts at 8:00 AM on specific days of the month on specific months.</span></span> <br/>                                                                                                       |
| [<span data-ttu-id="8623c-122">**ScheduleByMonthDayOfWeek**</span><span class="sxs-lookup"><span data-stu-id="8623c-122">**ScheduleByMonthDayOfWeek**</span></span>](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) | [<span data-ttu-id="8623c-123">**monthlyDayOfWeekScheduleType**</span><span class="sxs-lookup"><span data-stu-id="8623c-123">**monthlyDayOfWeekScheduleType**</span></span>](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) | <span data-ttu-id="8623c-124">指定在每月一周的排程上啟動工作的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="8623c-124">Specifies a trigger that starts a job on a monthly day-of-week schedule.</span></span> <span data-ttu-id="8623c-125">例如，工作會在一周的特定日子、每月的周數，以及當年的月份開始。</span><span class="sxs-lookup"><span data-stu-id="8623c-125">For example, the task starts on specific days of the week, weeks of the month, and months of the year.</span></span> <br/>                                               |
| [<span data-ttu-id="8623c-126">**ScheduleByWeek**</span><span class="sxs-lookup"><span data-stu-id="8623c-126">**ScheduleByWeek**</span></span>](taskschedulerschema-schedulebyweek-calendartriggertype-element.md)                     | [<span data-ttu-id="8623c-127">**weeklyScheduleType**</span><span class="sxs-lookup"><span data-stu-id="8623c-127">**weeklyScheduleType**</span></span>](taskschedulerschema-weeklyscheduletype-complextype.md)                     | <span data-ttu-id="8623c-128">指定每週排程。</span><span class="sxs-lookup"><span data-stu-id="8623c-128">Specifies a weekly schedule.</span></span> <span data-ttu-id="8623c-129">例如，工作會在每週的特定一天或每隔一周的特定一天，于上午8:00 開始。</span><span class="sxs-lookup"><span data-stu-id="8623c-129">For example, the task starts at 8:00 AM on a specific day of the week every week or on a specific day of the week every other week.</span></span> <br/>                                                              |



## <a name="remarks"></a><span data-ttu-id="8623c-130">備註</span><span class="sxs-lookup"><span data-stu-id="8623c-130">Remarks</span></span>

<span data-ttu-id="8623c-131">除了這裡定義的子項目之外， [**CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md) 專案也會使用 [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) 複雜類型所定義的子項目。</span><span class="sxs-lookup"><span data-stu-id="8623c-131">In addition to the child element defined here, the [**CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md) element also uses the child elements defined by the [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="8623c-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="8623c-132">Requirements</span></span>



| <span data-ttu-id="8623c-133">需求</span><span class="sxs-lookup"><span data-stu-id="8623c-133">Requirement</span></span> | <span data-ttu-id="8623c-134">值</span><span class="sxs-lookup"><span data-stu-id="8623c-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="8623c-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8623c-135">Minimum supported client</span></span><br/> | <span data-ttu-id="8623c-136">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8623c-136">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="8623c-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8623c-137">Minimum supported server</span></span><br/> | <span data-ttu-id="8623c-138">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8623c-138">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8623c-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8623c-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8623c-140">工作排程器架構複雜類型</span><span class="sxs-lookup"><span data-stu-id="8623c-140">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="8623c-141">工作排程器</span><span class="sxs-lookup"><span data-stu-id="8623c-141">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





