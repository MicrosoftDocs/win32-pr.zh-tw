---
title: 星期五 (daysOfWeekType) 元素
description: 指定工作在星期五執行。
ms.assetid: bff85911-d354-4954-8c69-7b6f2ca312d3
keywords:
- 星期五元素工作排程器
topic_type:
- apiref
api_name:
- Friday
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 951142e7e925ea71ef1f833be4421351aaea3b35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105222"
---
# <a name="friday-daysofweektype-element"></a><span data-ttu-id="0e5f2-104">星期五 (daysOfWeekType) 元素</span><span class="sxs-lookup"><span data-stu-id="0e5f2-104">Friday (daysOfWeekType) Element</span></span>

<span data-ttu-id="0e5f2-105">指定工作在星期五執行。</span><span class="sxs-lookup"><span data-stu-id="0e5f2-105">Specifies that the task runs on Friday.</span></span>

``` syntax
<xs:element name="Friday">
    <xs:complexType />
</xs:element>
```

<span data-ttu-id="0e5f2-106">**星期五** 元素是由 [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="0e5f2-106">The **Friday** element is defined by the [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="0e5f2-107">父元素</span><span class="sxs-lookup"><span data-stu-id="0e5f2-107">Parent element</span></span>



| <span data-ttu-id="0e5f2-108">元素</span><span class="sxs-lookup"><span data-stu-id="0e5f2-108">Element</span></span>                                                                                                                  | <span data-ttu-id="0e5f2-109">衍生自</span><span class="sxs-lookup"><span data-stu-id="0e5f2-109">Derived from</span></span>                                                             | <span data-ttu-id="0e5f2-110">Description</span><span class="sxs-lookup"><span data-stu-id="0e5f2-110">Description</span></span>                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0e5f2-111">**DaysOfWeek (monthlyDayOfWeekScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="0e5f2-111">**DaysOfWeek (monthlyDayOfWeekScheduleType)**</span></span>](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="0e5f2-112">**daysOfWeekType**</span><span class="sxs-lookup"><span data-stu-id="0e5f2-112">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md) | <span data-ttu-id="0e5f2-113">指定工作在一周中的哪幾天執行一周的每月日排程。</span><span class="sxs-lookup"><span data-stu-id="0e5f2-113">Specifies the days of the week in which the task runs for a monthly day-of-week schedule.</span></span><br/> |
| [<span data-ttu-id="0e5f2-114">**DaysOfWeek (weeklyScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="0e5f2-114">**DaysOfWeek (weeklyScheduleType)**</span></span>](taskschedulerschema-daysofweek-weeklyscheduletype-element.md)                     | [<span data-ttu-id="0e5f2-115">**daysOfWeekType**</span><span class="sxs-lookup"><span data-stu-id="0e5f2-115">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md) | <span data-ttu-id="0e5f2-116">指定每週排程執行工作的天數。</span><span class="sxs-lookup"><span data-stu-id="0e5f2-116">Specifies the days of the week in which the task runs for a weekly schedule.</span></span><br/>              |



## <a name="examples"></a><span data-ttu-id="0e5f2-117">範例</span><span class="sxs-lookup"><span data-stu-id="0e5f2-117">Examples</span></span>

<span data-ttu-id="0e5f2-118">下列 XML 會定義在星期五開始工作的星期幾行事曆。</span><span class="sxs-lookup"><span data-stu-id="0e5f2-118">The following XML defines a day of week calendar that starts a task on Friday.</span></span>


```XML
<DaysOfWeek>
    <Friday/>
</DaysOfWeek>
```



## <a name="requirements"></a><span data-ttu-id="0e5f2-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="0e5f2-119">Requirements</span></span>



| <span data-ttu-id="0e5f2-120">需求</span><span class="sxs-lookup"><span data-stu-id="0e5f2-120">Requirement</span></span> | <span data-ttu-id="0e5f2-121">值</span><span class="sxs-lookup"><span data-stu-id="0e5f2-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0e5f2-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0e5f2-122">Minimum supported client</span></span><br/> | <span data-ttu-id="0e5f2-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0e5f2-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="0e5f2-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0e5f2-124">Minimum supported server</span></span><br/> | <span data-ttu-id="0e5f2-125">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0e5f2-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0e5f2-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0e5f2-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e5f2-127">工作排程器架構元素</span><span class="sxs-lookup"><span data-stu-id="0e5f2-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="0e5f2-128">工作排程器</span><span class="sxs-lookup"><span data-stu-id="0e5f2-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





