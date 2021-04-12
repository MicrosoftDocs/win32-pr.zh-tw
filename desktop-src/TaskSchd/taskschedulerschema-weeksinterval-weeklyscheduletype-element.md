---
title: WeeksInterval (weeklyScheduleType) 元素
description: 指定排程中周之間的間隔。
ms.assetid: 6cbf1e7e-a695-4012-97fd-fe3360c362c4
keywords:
- WeeksInterval 元素工作排程器
topic_type:
- apiref
api_name:
- WeeksInterval
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 747ca4b73ff18bdb3e29d8b909d72b8d2367d89b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385101"
---
# <a name="weeksinterval-weeklyscheduletype-element"></a><span data-ttu-id="b7b58-104">WeeksInterval (weeklyScheduleType) 元素</span><span class="sxs-lookup"><span data-stu-id="b7b58-104">WeeksInterval (weeklyScheduleType) Element</span></span>

<span data-ttu-id="b7b58-105">指定排程中周之間的間隔。</span><span class="sxs-lookup"><span data-stu-id="b7b58-105">Specifies the interval between the weeks in the schedule.</span></span>

``` syntax
<xs:element name="WeeksInterval"
    minOccurs="0"
>
    <xs:simpleType>
        <xs:restriction
            base="unsignedByte"
        >
            <xs:minInclusive
                value="1"
             />
            <xs:maxInclusive
                value="52"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="b7b58-106">元素是由 [**weeklyScheduleType**](taskschedulerschema-weeklyscheduletype-complextype.md) 複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="b7b58-106">The element is defined by the [**weeklyScheduleType**](taskschedulerschema-weeklyscheduletype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="b7b58-107">父元素</span><span class="sxs-lookup"><span data-stu-id="b7b58-107">Parent element</span></span>



| <span data-ttu-id="b7b58-108">元素</span><span class="sxs-lookup"><span data-stu-id="b7b58-108">Element</span></span>                                                                                  | <span data-ttu-id="b7b58-109">衍生自</span><span class="sxs-lookup"><span data-stu-id="b7b58-109">Derived from</span></span>                                                                     | <span data-ttu-id="b7b58-110">Description</span><span class="sxs-lookup"><span data-stu-id="b7b58-110">Description</span></span>                             |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|-----------------------------------------|
| [<span data-ttu-id="b7b58-111">**ScheduleByWeek**</span><span class="sxs-lookup"><span data-stu-id="b7b58-111">**ScheduleByWeek**</span></span>](taskschedulerschema-schedulebyweek-calendartriggertype-element.md) | [<span data-ttu-id="b7b58-112">**weeklyScheduleType**</span><span class="sxs-lookup"><span data-stu-id="b7b58-112">**weeklyScheduleType**</span></span>](taskschedulerschema-weeklyscheduletype-complextype.md) | <span data-ttu-id="b7b58-113">指定每週排程。</span><span class="sxs-lookup"><span data-stu-id="b7b58-113">Specifies a weekly schedule.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="b7b58-114">備註</span><span class="sxs-lookup"><span data-stu-id="b7b58-114">Remarks</span></span>

<span data-ttu-id="b7b58-115">針對腳本開發，每週間隔會使用 [**WeeklyTrigger. WeeksInterval**](weeklytrigger-weeksinterval.md) 屬性來指定。</span><span class="sxs-lookup"><span data-stu-id="b7b58-115">For scripting development, the weekly interval is specified using the [**WeeklyTrigger.WeeksInterval**](weeklytrigger-weeksinterval.md) property.</span></span>

<span data-ttu-id="b7b58-116">針對 c + + 開發，每週間隔是使用 [**IWeeklyTrigger：： WeeksInterval**](/windows/desktop/api/taskschd/nf-taskschd-iweeklytrigger-get_weeksinterval) 屬性來指定。</span><span class="sxs-lookup"><span data-stu-id="b7b58-116">For C++ development, the weekly interval is specified using the [**IWeeklyTrigger::WeeksInterval**](/windows/desktop/api/taskschd/nf-taskschd-iweeklytrigger-get_weeksinterval) property.</span></span>

## <a name="examples"></a><span data-ttu-id="b7b58-117">範例</span><span class="sxs-lookup"><span data-stu-id="b7b58-117">Examples</span></span>

<span data-ttu-id="b7b58-118">下列 XML 定義每週的行事曆觸發程式，從星期一到星期五的上午 8:00 ( 開始工作) 。</span><span class="sxs-lookup"><span data-stu-id="b7b58-118">The following XML defines a weekly calendar trigger that starts a task Monday through Friday ( at 8:00 AM) every week.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="b7b58-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="b7b58-119">Requirements</span></span>



| <span data-ttu-id="b7b58-120">需求</span><span class="sxs-lookup"><span data-stu-id="b7b58-120">Requirement</span></span> | <span data-ttu-id="b7b58-121">值</span><span class="sxs-lookup"><span data-stu-id="b7b58-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b7b58-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b7b58-122">Minimum supported client</span></span><br/> | <span data-ttu-id="b7b58-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b7b58-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b7b58-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b7b58-124">Minimum supported server</span></span><br/> | <span data-ttu-id="b7b58-125">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b7b58-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b7b58-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b7b58-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7b58-127">工作排程器架構元素</span><span class="sxs-lookup"><span data-stu-id="b7b58-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="b7b58-128">工作排程器</span><span class="sxs-lookup"><span data-stu-id="b7b58-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





