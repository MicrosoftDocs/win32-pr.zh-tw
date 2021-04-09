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
# <a name="august-monthstype-element"></a><span data-ttu-id="e14bc-104">八月 (monthsType) 元素</span><span class="sxs-lookup"><span data-stu-id="e14bc-104">August (monthsType) Element</span></span>

<span data-ttu-id="e14bc-105">指定工作在8月執行。</span><span class="sxs-lookup"><span data-stu-id="e14bc-105">Specifies that the task runs in August.</span></span>

``` syntax
<xs:element name="August">
    <xs:complexType />
</xs:element>
```

<span data-ttu-id="e14bc-106">**八月** 元素是由 [**monthsType**](taskschedulerschema-monthstype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="e14bc-106">The **August** element is defined by the [**monthsType**](taskschedulerschema-monthstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="e14bc-107">父元素</span><span class="sxs-lookup"><span data-stu-id="e14bc-107">Parent element</span></span>



| <span data-ttu-id="e14bc-108">元素</span><span class="sxs-lookup"><span data-stu-id="e14bc-108">Element</span></span>                                                                                                          | <span data-ttu-id="e14bc-109">衍生自</span><span class="sxs-lookup"><span data-stu-id="e14bc-109">Derived from</span></span>                                                     | <span data-ttu-id="e14bc-110">Description</span><span class="sxs-lookup"><span data-stu-id="e14bc-110">Description</span></span>                                                                                                |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e14bc-111">**MonthlyDayOfWeekScheduleType) 的月份 (**</span><span class="sxs-lookup"><span data-stu-id="e14bc-111">**Months (monthlyDayOfWeekScheduleType)**</span></span>](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="e14bc-112">**monthsType**</span><span class="sxs-lookup"><span data-stu-id="e14bc-112">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="e14bc-113">指定在一年中的幾個月，工作會在一年中執行一周的每月日排程。</span><span class="sxs-lookup"><span data-stu-id="e14bc-113">Specifies the months of the year during which the task runs for a monthly day-of-week schedule.</span></span><br/> |
| [<span data-ttu-id="e14bc-114">**MonthlyScheduleType) 的月份 (**</span><span class="sxs-lookup"><span data-stu-id="e14bc-114">**Months (monthlyScheduleType)**</span></span>](taskschedulerschema-months-monthlyscheduletype-element.md)                   | [<span data-ttu-id="e14bc-115">**monthsType**</span><span class="sxs-lookup"><span data-stu-id="e14bc-115">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="e14bc-116">指定執行每月排程之工作的年度月份。</span><span class="sxs-lookup"><span data-stu-id="e14bc-116">Specifies the months of the year during which the task runs for a monthly schedule.</span></span><br/>             |



## <a name="examples"></a><span data-ttu-id="e14bc-117">範例</span><span class="sxs-lookup"><span data-stu-id="e14bc-117">Examples</span></span>

<span data-ttu-id="e14bc-118">下列 XML 會定義在8月執行工作的月份行事曆。</span><span class="sxs-lookup"><span data-stu-id="e14bc-118">The following XML defines a months calendar that runs the task in August.</span></span>


```XML
<Months>
    <August/>
</Months>
```



## <a name="requirements"></a><span data-ttu-id="e14bc-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="e14bc-119">Requirements</span></span>



| <span data-ttu-id="e14bc-120">需求</span><span class="sxs-lookup"><span data-stu-id="e14bc-120">Requirement</span></span> | <span data-ttu-id="e14bc-121">值</span><span class="sxs-lookup"><span data-stu-id="e14bc-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e14bc-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e14bc-122">Minimum supported client</span></span><br/> | <span data-ttu-id="e14bc-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e14bc-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e14bc-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e14bc-124">Minimum supported server</span></span><br/> | <span data-ttu-id="e14bc-125">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e14bc-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e14bc-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e14bc-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e14bc-127">工作排程器架構元素</span><span class="sxs-lookup"><span data-stu-id="e14bc-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="e14bc-128">工作排程器</span><span class="sxs-lookup"><span data-stu-id="e14bc-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





