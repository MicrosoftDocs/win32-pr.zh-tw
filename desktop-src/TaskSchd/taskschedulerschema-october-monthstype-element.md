---
title: 十月 (monthsType) 元素
description: 指定工作在十月執行。
ms.assetid: 62c8bb3e-a70f-45b8-8d80-7a7eef9dfaeb
keywords:
- 十月元素工作排程器
topic_type:
- apiref
api_name:
- October
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 79bf2a2dde46341f48808342ab6aefb78863524b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106361"
---
# <a name="october-monthstype-element"></a><span data-ttu-id="18d92-104">十月 (monthsType) 元素</span><span class="sxs-lookup"><span data-stu-id="18d92-104">October (monthsType) Element</span></span>

<span data-ttu-id="18d92-105">指定工作在十月執行。</span><span class="sxs-lookup"><span data-stu-id="18d92-105">Specifies that the task runs in October.</span></span>

``` syntax
<xs:element name="October">
    <xs:complexType />
</xs:element>
```

<span data-ttu-id="18d92-106">**十月** 元素是由 [**monthsType**](taskschedulerschema-monthstype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="18d92-106">The **October** element is defined by the [**monthsType**](taskschedulerschema-monthstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="18d92-107">父元素</span><span class="sxs-lookup"><span data-stu-id="18d92-107">Parent element</span></span>



| <span data-ttu-id="18d92-108">元素</span><span class="sxs-lookup"><span data-stu-id="18d92-108">Element</span></span>                                                                                                          | <span data-ttu-id="18d92-109">衍生自</span><span class="sxs-lookup"><span data-stu-id="18d92-109">Derived from</span></span>                                                     | <span data-ttu-id="18d92-110">Description</span><span class="sxs-lookup"><span data-stu-id="18d92-110">Description</span></span>                                                                                                |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="18d92-111">**MonthlyDayOfWeekScheduleType) 的月份 (**</span><span class="sxs-lookup"><span data-stu-id="18d92-111">**Months (monthlyDayOfWeekScheduleType)**</span></span>](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="18d92-112">**monthsType**</span><span class="sxs-lookup"><span data-stu-id="18d92-112">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="18d92-113">指定在一年中的幾個月，工作會在一年中執行一周的每月日排程。</span><span class="sxs-lookup"><span data-stu-id="18d92-113">Specifies the months of the year during which the task runs for a monthly day-of-week schedule.</span></span><br/> |
| [<span data-ttu-id="18d92-114">**MonthlyScheduleType) 的月份 (**</span><span class="sxs-lookup"><span data-stu-id="18d92-114">**Months (monthlyScheduleType)**</span></span>](taskschedulerschema-months-monthlyscheduletype-element.md)                   | [<span data-ttu-id="18d92-115">**monthsType**</span><span class="sxs-lookup"><span data-stu-id="18d92-115">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="18d92-116">指定執行每月排程之工作的年度月份。</span><span class="sxs-lookup"><span data-stu-id="18d92-116">Specifies the months of the year during which the task runs for a monthly schedule.</span></span><br/>             |



## <a name="examples"></a><span data-ttu-id="18d92-117">範例</span><span class="sxs-lookup"><span data-stu-id="18d92-117">Examples</span></span>

<span data-ttu-id="18d92-118">下列 XML 會定義在10月執行工作的月份行事曆。</span><span class="sxs-lookup"><span data-stu-id="18d92-118">The following XML defines a months calendar that runs the task in October.</span></span>


```XML
<Months>
    <October/>
</Months>
```



## <a name="requirements"></a><span data-ttu-id="18d92-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="18d92-119">Requirements</span></span>



| <span data-ttu-id="18d92-120">需求</span><span class="sxs-lookup"><span data-stu-id="18d92-120">Requirement</span></span> | <span data-ttu-id="18d92-121">值</span><span class="sxs-lookup"><span data-stu-id="18d92-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="18d92-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="18d92-122">Minimum supported client</span></span><br/> | <span data-ttu-id="18d92-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="18d92-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="18d92-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="18d92-124">Minimum supported server</span></span><br/> | <span data-ttu-id="18d92-125">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="18d92-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="18d92-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="18d92-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18d92-127">工作排程器架構元素</span><span class="sxs-lookup"><span data-stu-id="18d92-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="18d92-128">工作排程器</span><span class="sxs-lookup"><span data-stu-id="18d92-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





