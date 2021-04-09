---
title: 星期六 (daysOfWeekType) 元素
description: 指定工作在星期六執行。
ms.assetid: def26a72-c143-466a-b5b0-6105078afffa
keywords:
- 星期六元素工作排程器
topic_type:
- apiref
api_name:
- Saturday
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1b5f7cb36002b2add64cdea541caa2fd28df37ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686256"
---
# <a name="saturday-daysofweektype-element"></a><span data-ttu-id="6303d-104">星期六 (daysOfWeekType) 元素</span><span class="sxs-lookup"><span data-stu-id="6303d-104">Saturday (daysOfWeekType) Element</span></span>

<span data-ttu-id="6303d-105">指定工作在星期六執行。</span><span class="sxs-lookup"><span data-stu-id="6303d-105">Specifies that the task runs on Saturday.</span></span>

``` syntax
<xs:element name="Saturday">
    <xs:complexType />
</xs:element>
```

<span data-ttu-id="6303d-106">**星期六** 元素是由 [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="6303d-106">The **Saturday** element is defined by the [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="6303d-107">父元素</span><span class="sxs-lookup"><span data-stu-id="6303d-107">Parent element</span></span>



| <span data-ttu-id="6303d-108">元素</span><span class="sxs-lookup"><span data-stu-id="6303d-108">Element</span></span>                                                                                                                  | <span data-ttu-id="6303d-109">衍生自</span><span class="sxs-lookup"><span data-stu-id="6303d-109">Derived from</span></span>                                                             | <span data-ttu-id="6303d-110">Description</span><span class="sxs-lookup"><span data-stu-id="6303d-110">Description</span></span>                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6303d-111">**DaysOfWeek (monthlyDayOfWeekScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="6303d-111">**DaysOfWeek (monthlyDayOfWeekScheduleType)**</span></span>](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="6303d-112">**daysOfWeekType**</span><span class="sxs-lookup"><span data-stu-id="6303d-112">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md) | <span data-ttu-id="6303d-113">指定工作在一周中的哪幾天執行一周的每月日排程。</span><span class="sxs-lookup"><span data-stu-id="6303d-113">Specifies the days of the week in which the task runs for a monthly day-of-week schedule.</span></span><br/> |
| [<span data-ttu-id="6303d-114">**DaysOfWeek (weeklyScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="6303d-114">**DaysOfWeek (weeklyScheduleType)**</span></span>](taskschedulerschema-daysofweek-weeklyscheduletype-element.md)                     | [<span data-ttu-id="6303d-115">**daysOfWeekType**</span><span class="sxs-lookup"><span data-stu-id="6303d-115">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md) | <span data-ttu-id="6303d-116">指定每週排程執行工作的天數。</span><span class="sxs-lookup"><span data-stu-id="6303d-116">Specifies the days of the week in which the task runs for a weekly schedule.</span></span><br/>              |



## <a name="examples"></a><span data-ttu-id="6303d-117">範例</span><span class="sxs-lookup"><span data-stu-id="6303d-117">Examples</span></span>

<span data-ttu-id="6303d-118">下列 XML 會定義在星期六開始工作的星期幾行事曆。</span><span class="sxs-lookup"><span data-stu-id="6303d-118">The following XML defines a day of week calendar that starts a task on Saturday.</span></span>


```XML
<DaysOfWeek>
    <Saturday/>
</DaysOfWeek>
```



## <a name="requirements"></a><span data-ttu-id="6303d-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="6303d-119">Requirements</span></span>



| <span data-ttu-id="6303d-120">需求</span><span class="sxs-lookup"><span data-stu-id="6303d-120">Requirement</span></span> | <span data-ttu-id="6303d-121">值</span><span class="sxs-lookup"><span data-stu-id="6303d-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6303d-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6303d-122">Minimum supported client</span></span><br/> | <span data-ttu-id="6303d-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6303d-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="6303d-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6303d-124">Minimum supported server</span></span><br/> | <span data-ttu-id="6303d-125">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6303d-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6303d-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6303d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6303d-127">工作排程器架構元素</span><span class="sxs-lookup"><span data-stu-id="6303d-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="6303d-128">工作排程器</span><span class="sxs-lookup"><span data-stu-id="6303d-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





