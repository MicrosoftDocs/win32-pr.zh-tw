---
title: 星期四 (daysOfWeekType) 元素
description: 指定工作在星期四執行。
ms.assetid: 01d0e7e8-7135-4f43-9d8f-b50c002b93bc
keywords:
- 星期四元素工作排程器
topic_type:
- apiref
api_name:
- Thursday
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 12b1fb602411a9e4562a044b044e43de4800f239
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969609"
---
# <a name="thursday-daysofweektype-element"></a><span data-ttu-id="dd6db-104">星期四 (daysOfWeekType) 元素</span><span class="sxs-lookup"><span data-stu-id="dd6db-104">Thursday (daysOfWeekType) Element</span></span>

<span data-ttu-id="dd6db-105">指定工作在星期四執行。</span><span class="sxs-lookup"><span data-stu-id="dd6db-105">Specifies that the task runs on Thursday.</span></span>

``` syntax
<xs:element name="Thursday">
    <xs:complexType />
</xs:element>
```

<span data-ttu-id="dd6db-106">**星期四** 元素是由 [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="dd6db-106">The **Thursday** element is defined by the [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="dd6db-107">父元素</span><span class="sxs-lookup"><span data-stu-id="dd6db-107">Parent element</span></span>



| <span data-ttu-id="dd6db-108">元素</span><span class="sxs-lookup"><span data-stu-id="dd6db-108">Element</span></span>                                                                                                                  | <span data-ttu-id="dd6db-109">衍生自</span><span class="sxs-lookup"><span data-stu-id="dd6db-109">Derived from</span></span>                                                             | <span data-ttu-id="dd6db-110">Description</span><span class="sxs-lookup"><span data-stu-id="dd6db-110">Description</span></span>                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dd6db-111">**DaysOfWeek (monthlyDayOfWeekScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="dd6db-111">**DaysOfWeek (monthlyDayOfWeekScheduleType)**</span></span>](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="dd6db-112">**daysOfWeekType**</span><span class="sxs-lookup"><span data-stu-id="dd6db-112">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md) | <span data-ttu-id="dd6db-113">指定工作在一周中的哪幾天執行一周的每月日排程。</span><span class="sxs-lookup"><span data-stu-id="dd6db-113">Specifies the days of the week in which the task runs for a monthly day-of-week schedule.</span></span><br/> |
| [<span data-ttu-id="dd6db-114">**DaysOfWeek (weeklyScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="dd6db-114">**DaysOfWeek (weeklyScheduleType)**</span></span>](taskschedulerschema-daysofweek-weeklyscheduletype-element.md)                     | [<span data-ttu-id="dd6db-115">**daysOfWeekType**</span><span class="sxs-lookup"><span data-stu-id="dd6db-115">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md) | <span data-ttu-id="dd6db-116">指定每週排程執行工作的天數。</span><span class="sxs-lookup"><span data-stu-id="dd6db-116">Specifies the days of the week in which the task runs for a weekly schedule.</span></span><br/>              |



## <a name="examples"></a><span data-ttu-id="dd6db-117">範例</span><span class="sxs-lookup"><span data-stu-id="dd6db-117">Examples</span></span>

<span data-ttu-id="dd6db-118">下列 XML 會定義在星期四開始工作的星期幾行事曆。</span><span class="sxs-lookup"><span data-stu-id="dd6db-118">The following XML defines a day of week calendar that starts a task on Thursday.</span></span>


```XML
<DaysOfWeek>
    <Thursday/>
</DaysOfWeek>
```



## <a name="requirements"></a><span data-ttu-id="dd6db-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="dd6db-119">Requirements</span></span>



| <span data-ttu-id="dd6db-120">需求</span><span class="sxs-lookup"><span data-stu-id="dd6db-120">Requirement</span></span> | <span data-ttu-id="dd6db-121">值</span><span class="sxs-lookup"><span data-stu-id="dd6db-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="dd6db-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="dd6db-122">Minimum supported client</span></span><br/> | <span data-ttu-id="dd6db-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dd6db-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="dd6db-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="dd6db-124">Minimum supported server</span></span><br/> | <span data-ttu-id="dd6db-125">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dd6db-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="dd6db-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dd6db-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd6db-127">工作排程器架構元素</span><span class="sxs-lookup"><span data-stu-id="dd6db-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="dd6db-128">工作排程器</span><span class="sxs-lookup"><span data-stu-id="dd6db-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





