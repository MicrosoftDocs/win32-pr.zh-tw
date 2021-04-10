---
title: DaysInterval (dailyScheduleType) 元素
description: 指定排程中天數之間的間隔。
ms.assetid: 495ea1c0-37eb-4b12-8241-bfc6489e33ed
keywords:
- DaysInterval 元素工作排程器
topic_type:
- apiref
api_name:
- DaysInterval
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 97b50581aa4825b31983a234a5eb47ff7b7b7e06
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934019"
---
# <a name="daysinterval-dailyscheduletype-element"></a><span data-ttu-id="f1acd-104">DaysInterval (dailyScheduleType) 元素</span><span class="sxs-lookup"><span data-stu-id="f1acd-104">DaysInterval (dailyScheduleType) Element</span></span>

<span data-ttu-id="f1acd-105">指定排程中天數之間的間隔。</span><span class="sxs-lookup"><span data-stu-id="f1acd-105">Specifies the interval between the days in the schedule.</span></span>

``` syntax
<xs:element name="DaysInterval"
    minOccurs="0"
>
    <xs:simpleType>
        <xs:restriction
            base="unsignedInt"
        >
            <xs:minInclusive
                value="1"
             />
            <xs:maxInclusive
                value="365"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="f1acd-106">元素是由 [**dailyScheduleType**](taskschedulerschema-dailyscheduletype-complextype.md) 複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="f1acd-106">The element is defined by the [**dailyScheduleType**](taskschedulerschema-dailyscheduletype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="f1acd-107">父元素</span><span class="sxs-lookup"><span data-stu-id="f1acd-107">Parent element</span></span>



| <span data-ttu-id="f1acd-108">元素</span><span class="sxs-lookup"><span data-stu-id="f1acd-108">Element</span></span>                                                                                | <span data-ttu-id="f1acd-109">衍生自</span><span class="sxs-lookup"><span data-stu-id="f1acd-109">Derived from</span></span>                                                                   | <span data-ttu-id="f1acd-110">Description</span><span class="sxs-lookup"><span data-stu-id="f1acd-110">Description</span></span>                            |
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|----------------------------------------|
| [<span data-ttu-id="f1acd-111">**ScheduleByDay**</span><span class="sxs-lookup"><span data-stu-id="f1acd-111">**ScheduleByDay**</span></span>](taskschedulerschema-schedulebyday-calendartriggertype-element.md) | [<span data-ttu-id="f1acd-112">**dailyScheduleType**</span><span class="sxs-lookup"><span data-stu-id="f1acd-112">**dailyScheduleType**</span></span>](taskschedulerschema-dailyscheduletype-complextype.md) | <span data-ttu-id="f1acd-113">指定每日排程。</span><span class="sxs-lookup"><span data-stu-id="f1acd-113">Specifies a daily schedule.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="f1acd-114">備註</span><span class="sxs-lookup"><span data-stu-id="f1acd-114">Remarks</span></span>

<span data-ttu-id="f1acd-115">針對腳本開發，每日觸發程式的天數間隔是由 [**DailyTrigger. DaysInterval**](dailytrigger-daysinterval.md) 屬性所指定。</span><span class="sxs-lookup"><span data-stu-id="f1acd-115">For script development, the days interval for a daily trigger is specified by the [**DailyTrigger.DaysInterval**](dailytrigger-daysinterval.md) property.</span></span>

<span data-ttu-id="f1acd-116">針對 c + + 開發，每日觸發程式的天數間隔是由 [**IDailyTrigger：:D aysinterval**](/windows/desktop/api/taskschd/nf-taskschd-idailytrigger-get_daysinterval) 屬性所指定。</span><span class="sxs-lookup"><span data-stu-id="f1acd-116">For C++ development, the days interval for a daily trigger is specified by the [**IDailyTrigger::DaysInterval**](/windows/desktop/api/taskschd/nf-taskschd-idailytrigger-get_daysinterval) property.</span></span>

## <a name="examples"></a><span data-ttu-id="f1acd-117">範例</span><span class="sxs-lookup"><span data-stu-id="f1acd-117">Examples</span></span>

<span data-ttu-id="f1acd-118">下列 XML 會定義每日啟動工作的每日行事曆觸發程式。</span><span class="sxs-lookup"><span data-stu-id="f1acd-118">The following XML defines a daily calendar trigger that starts the task every day.</span></span>


```XML
<CalendarTrigger>
    <StartBoundary>2005-01-01T00:00:00</StartBoundary>
    <EndBounadry>2007-01-01T00:00:00</EndBoundary>
    <ScheduleByDay>
        <DaysInterval>1</DaysInterval>
    </ScheduleByDay>
</CalendarTrigger>
```



<span data-ttu-id="f1acd-119">如需指定每日排程之工作的 XML 完整範例，請參閱 [ (XML) 的每日觸發程式範例 ](daily-trigger-example--xml-.md)。</span><span class="sxs-lookup"><span data-stu-id="f1acd-119">For a complete example of the XML for a task that specifies a daily schedule, see [Daily Trigger Example (XML)](daily-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f1acd-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="f1acd-120">Requirements</span></span>



| <span data-ttu-id="f1acd-121">需求</span><span class="sxs-lookup"><span data-stu-id="f1acd-121">Requirement</span></span> | <span data-ttu-id="f1acd-122">值</span><span class="sxs-lookup"><span data-stu-id="f1acd-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f1acd-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f1acd-123">Minimum supported client</span></span><br/> | <span data-ttu-id="f1acd-124">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f1acd-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f1acd-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f1acd-125">Minimum supported server</span></span><br/> | <span data-ttu-id="f1acd-126">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f1acd-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f1acd-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f1acd-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1acd-128">工作排程器架構元素</span><span class="sxs-lookup"><span data-stu-id="f1acd-128">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="f1acd-129">工作排程器</span><span class="sxs-lookup"><span data-stu-id="f1acd-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





