---
title: 星期日 (daysOfWeekType) 元素
description: 指定工作在星期日執行。
ms.assetid: 856db869-2273-4bb8-88c8-c126bb16c87b
keywords:
- 星期日元素工作排程器
topic_type:
- apiref
api_name:
- Sunday
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 40efba31b392da5959853feeb1cae567cee25cc7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105353"
---
# <a name="sunday-daysofweektype-element"></a><span data-ttu-id="2ca51-104">星期日 (daysOfWeekType) 元素</span><span class="sxs-lookup"><span data-stu-id="2ca51-104">Sunday (daysOfWeekType) Element</span></span>

<span data-ttu-id="2ca51-105">指定工作在星期日執行。</span><span class="sxs-lookup"><span data-stu-id="2ca51-105">Specifies that the task runs on Sunday.</span></span>

``` syntax
<xs:element name="Sunday">
    <xs:complexType />
</xs:element>
```

<span data-ttu-id="2ca51-106">**星期日** 元素是由 [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="2ca51-106">The **Sunday** element is defined by the [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="2ca51-107">父元素</span><span class="sxs-lookup"><span data-stu-id="2ca51-107">Parent element</span></span>



| <span data-ttu-id="2ca51-108">元素</span><span class="sxs-lookup"><span data-stu-id="2ca51-108">Element</span></span>                                                                                                                  | <span data-ttu-id="2ca51-109">衍生自</span><span class="sxs-lookup"><span data-stu-id="2ca51-109">Derived from</span></span>                                                             | <span data-ttu-id="2ca51-110">Description</span><span class="sxs-lookup"><span data-stu-id="2ca51-110">Description</span></span>                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2ca51-111">**DaysOfWeek (monthlyDayOfWeekScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="2ca51-111">**DaysOfWeek (monthlyDayOfWeekScheduleType)**</span></span>](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="2ca51-112">**daysOfWeekType**</span><span class="sxs-lookup"><span data-stu-id="2ca51-112">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md) | <span data-ttu-id="2ca51-113">指定工作在一周中的哪幾天執行一周的每月日排程。</span><span class="sxs-lookup"><span data-stu-id="2ca51-113">Specifies the days of the week in which the task runs for a monthly day-of-week schedule.</span></span><br/> |
| [<span data-ttu-id="2ca51-114">**DaysOfWeek (weeklyScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="2ca51-114">**DaysOfWeek (weeklyScheduleType)**</span></span>](taskschedulerschema-daysofweek-weeklyscheduletype-element.md)                     | [<span data-ttu-id="2ca51-115">**daysOfWeekType**</span><span class="sxs-lookup"><span data-stu-id="2ca51-115">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md) | <span data-ttu-id="2ca51-116">指定每週排程執行工作的天數。</span><span class="sxs-lookup"><span data-stu-id="2ca51-116">Specifies the days of the week in which the task runs for a weekly schedule.</span></span><br/>              |



## <a name="examples"></a><span data-ttu-id="2ca51-117">範例</span><span class="sxs-lookup"><span data-stu-id="2ca51-117">Examples</span></span>

<span data-ttu-id="2ca51-118">下列 XML 會定義在星期日啟動工作的星期幾行事曆。</span><span class="sxs-lookup"><span data-stu-id="2ca51-118">The following XML defines a day of week calendar that starts a task on Sunday.</span></span>


```XML
<DaysOfWeek>
    <Sunday/>
</DaysOfWeek>
```



## <a name="requirements"></a><span data-ttu-id="2ca51-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="2ca51-119">Requirements</span></span>



| <span data-ttu-id="2ca51-120">需求</span><span class="sxs-lookup"><span data-stu-id="2ca51-120">Requirement</span></span> | <span data-ttu-id="2ca51-121">值</span><span class="sxs-lookup"><span data-stu-id="2ca51-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="2ca51-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2ca51-122">Minimum supported client</span></span><br/> | <span data-ttu-id="2ca51-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2ca51-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="2ca51-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2ca51-124">Minimum supported server</span></span><br/> | <span data-ttu-id="2ca51-125">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2ca51-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2ca51-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2ca51-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ca51-127">工作排程器架構元素</span><span class="sxs-lookup"><span data-stu-id="2ca51-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="2ca51-128">工作排程器</span><span class="sxs-lookup"><span data-stu-id="2ca51-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





