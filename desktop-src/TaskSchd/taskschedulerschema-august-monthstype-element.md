---
title: 八月 (monthsType) 元素
description: 指定工作在8月執行。
ms.assetid: cd7e528c-d482-4bb4-a31f-fccdb19a441b
keywords:
- 八月元素工作排程器
topic_type:
- apiref
api_name:
- August
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4978ebd8f22da6e157461791c4c2000fce9db6ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843856"
---
# <a name="august-monthstype-element"></a><span data-ttu-id="71fac-104">八月 (monthsType) 元素</span><span class="sxs-lookup"><span data-stu-id="71fac-104">August (monthsType) Element</span></span>

<span data-ttu-id="71fac-105">指定工作在8月執行。</span><span class="sxs-lookup"><span data-stu-id="71fac-105">Specifies that the task runs in August.</span></span>

``` syntax
<xs:element name="August">
    <xs:complexType />
</xs:element>
```

<span data-ttu-id="71fac-106">**八月** 元素是由 [**monthsType**](taskschedulerschema-monthstype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="71fac-106">The **August** element is defined by the [**monthsType**](taskschedulerschema-monthstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="71fac-107">父元素</span><span class="sxs-lookup"><span data-stu-id="71fac-107">Parent element</span></span>



| <span data-ttu-id="71fac-108">元素</span><span class="sxs-lookup"><span data-stu-id="71fac-108">Element</span></span>                                                                                                          | <span data-ttu-id="71fac-109">衍生自</span><span class="sxs-lookup"><span data-stu-id="71fac-109">Derived from</span></span>                                                     | <span data-ttu-id="71fac-110">Description</span><span class="sxs-lookup"><span data-stu-id="71fac-110">Description</span></span>                                                                                                |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="71fac-111">**MonthlyDayOfWeekScheduleType) 的月份 (**</span><span class="sxs-lookup"><span data-stu-id="71fac-111">**Months (monthlyDayOfWeekScheduleType)**</span></span>](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="71fac-112">**monthsType**</span><span class="sxs-lookup"><span data-stu-id="71fac-112">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="71fac-113">指定在一年中的幾個月，工作會在一年中執行一周的每月日排程。</span><span class="sxs-lookup"><span data-stu-id="71fac-113">Specifies the months of the year during which the task runs for a monthly day-of-week schedule.</span></span><br/> |
| [<span data-ttu-id="71fac-114">**MonthlyScheduleType) 的月份 (**</span><span class="sxs-lookup"><span data-stu-id="71fac-114">**Months (monthlyScheduleType)**</span></span>](taskschedulerschema-months-monthlyscheduletype-element.md)                   | [<span data-ttu-id="71fac-115">**monthsType**</span><span class="sxs-lookup"><span data-stu-id="71fac-115">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="71fac-116">指定執行每月排程之工作的年度月份。</span><span class="sxs-lookup"><span data-stu-id="71fac-116">Specifies the months of the year during which the task runs for a monthly schedule.</span></span><br/>             |



## <a name="examples"></a><span data-ttu-id="71fac-117">範例</span><span class="sxs-lookup"><span data-stu-id="71fac-117">Examples</span></span>

<span data-ttu-id="71fac-118">下列 XML 會定義在8月執行工作的月份行事曆。</span><span class="sxs-lookup"><span data-stu-id="71fac-118">The following XML defines a months calendar that runs the task in August.</span></span>


```XML
<Months>
    <August/>
</Months>
```



## <a name="requirements"></a><span data-ttu-id="71fac-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="71fac-119">Requirements</span></span>



| <span data-ttu-id="71fac-120">需求</span><span class="sxs-lookup"><span data-stu-id="71fac-120">Requirement</span></span> | <span data-ttu-id="71fac-121">值</span><span class="sxs-lookup"><span data-stu-id="71fac-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="71fac-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="71fac-122">Minimum supported client</span></span><br/> | <span data-ttu-id="71fac-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="71fac-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="71fac-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="71fac-124">Minimum supported server</span></span><br/> | <span data-ttu-id="71fac-125">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="71fac-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="71fac-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="71fac-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71fac-127">工作排程器架構元素</span><span class="sxs-lookup"><span data-stu-id="71fac-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="71fac-128">工作排程器</span><span class="sxs-lookup"><span data-stu-id="71fac-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





