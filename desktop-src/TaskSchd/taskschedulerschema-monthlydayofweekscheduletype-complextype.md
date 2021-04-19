---
title: monthlyDayOfWeekScheduleType 複雜類型
description: 定義 ScheduleByMonthDayOfWeek 元素的子項目和排序資訊。
ms.assetid: fb4e5ba3-592b-47a4-bedf-5181d2b7a50f
keywords:
- monthlyDayOfWeekScheduleType 複雜類型工作排程器
topic_type:
- apiref
api_name:
- monthlyDayOfWeekScheduleType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 782715aed5cbf59a98e996bfa18fdd7c1022227a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969194"
---
# <a name="monthlydayofweekscheduletype-complex-type"></a><span data-ttu-id="edf0a-104">monthlyDayOfWeekScheduleType 複雜類型</span><span class="sxs-lookup"><span data-stu-id="edf0a-104">monthlyDayOfWeekScheduleType Complex Type</span></span>

<span data-ttu-id="edf0a-105">定義 [**ScheduleByMonthDayOfWeek**](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) 元素的子項目和排序資訊。</span><span class="sxs-lookup"><span data-stu-id="edf0a-105">Defines the child elements and sequencing information for the [**ScheduleByMonthDayOfWeek**](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) element.</span></span>

``` syntax
<xs:complexType name="monthlyDayOfWeekScheduleType">
    <xs:all>
        <xs:element name="Weeks"
            type="weeksType"
            minOccurs="0"
         />
        <xs:element name="DaysOfWeek"
            type="daysOfWeekType"
         />
        <xs:element name="Months"
            type="monthsType"
            minOccurs="0"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="edf0a-106">子元素</span><span class="sxs-lookup"><span data-stu-id="edf0a-106">Child elements</span></span>



| <span data-ttu-id="edf0a-107">元素</span><span class="sxs-lookup"><span data-stu-id="edf0a-107">Element</span></span>                                                                                   | <span data-ttu-id="edf0a-108">類型</span><span class="sxs-lookup"><span data-stu-id="edf0a-108">Type</span></span>                                                                     | <span data-ttu-id="edf0a-109">Description</span><span class="sxs-lookup"><span data-stu-id="edf0a-109">Description</span></span>                                                             |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [<span data-ttu-id="edf0a-110">**DaysOfWeek**</span><span class="sxs-lookup"><span data-stu-id="edf0a-110">**DaysOfWeek**</span></span>](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="edf0a-111">**daysOfWeekType**</span><span class="sxs-lookup"><span data-stu-id="edf0a-111">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md) | <span data-ttu-id="edf0a-112">指定工作執行的星期幾。</span><span class="sxs-lookup"><span data-stu-id="edf0a-112">Specifies the days of the week during which the task runs.</span></span><br/>   |
| [<span data-ttu-id="edf0a-113">**月**</span><span class="sxs-lookup"><span data-stu-id="edf0a-113">**Months**</span></span>](taskschedulerschema-months-monthlydayofweekscheduletype-element.md)         | [<span data-ttu-id="edf0a-114">**monthsType**</span><span class="sxs-lookup"><span data-stu-id="edf0a-114">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md)         | <span data-ttu-id="edf0a-115">指定執行工作的年份月份。</span><span class="sxs-lookup"><span data-stu-id="edf0a-115">Specifies the months of the year during which the task runs.</span></span><br/> |
| [<span data-ttu-id="edf0a-116">**星期**</span><span class="sxs-lookup"><span data-stu-id="edf0a-116">**Weeks**</span></span>](taskschedulerschema-weeks-monthlydayofweekscheduletype-element.md)           | [<span data-ttu-id="edf0a-117">**weeksType**</span><span class="sxs-lookup"><span data-stu-id="edf0a-117">**weeksType**</span></span>](taskschedulerschema-weekstype-complextype.md)           | <span data-ttu-id="edf0a-118">指定執行工作的月份周數。</span><span class="sxs-lookup"><span data-stu-id="edf0a-118">Specifies the weeks of the month during which the task runs.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="edf0a-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="edf0a-119">Requirements</span></span>



| <span data-ttu-id="edf0a-120">需求</span><span class="sxs-lookup"><span data-stu-id="edf0a-120">Requirement</span></span> | <span data-ttu-id="edf0a-121">值</span><span class="sxs-lookup"><span data-stu-id="edf0a-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="edf0a-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="edf0a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="edf0a-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="edf0a-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="edf0a-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="edf0a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="edf0a-125">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="edf0a-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="edf0a-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="edf0a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="edf0a-127">工作排程器架構複雜類型</span><span class="sxs-lookup"><span data-stu-id="edf0a-127">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="edf0a-128">工作排程器</span><span class="sxs-lookup"><span data-stu-id="edf0a-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





