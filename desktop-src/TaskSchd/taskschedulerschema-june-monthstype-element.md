---
title: 六月 (monthsType) 元素
description: 指定工作在六月執行。
ms.assetid: 15b0e8c2-4dc1-4ca3-99c5-bd9a36718904
keywords:
- 六月元素工作排程器
topic_type:
- apiref
api_name:
- June
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6e6c21834348a70033af69a71534c60c1b08d91a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686138"
---
# <a name="june-monthstype-element"></a><span data-ttu-id="476b2-104">六月 (monthsType) 元素</span><span class="sxs-lookup"><span data-stu-id="476b2-104">June (monthsType) Element</span></span>

<span data-ttu-id="476b2-105">指定工作在六月執行。</span><span class="sxs-lookup"><span data-stu-id="476b2-105">Specifies that the task runs in June.</span></span>

``` syntax
<xs:element name="June">
    <xs:complexType />
</xs:element>
```

<span data-ttu-id="476b2-106">**六月** 元素是由 [**monthsType**](taskschedulerschema-monthstype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="476b2-106">The **June** element is defined by the [**monthsType**](taskschedulerschema-monthstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="476b2-107">父元素</span><span class="sxs-lookup"><span data-stu-id="476b2-107">Parent element</span></span>



| <span data-ttu-id="476b2-108">元素</span><span class="sxs-lookup"><span data-stu-id="476b2-108">Element</span></span>                                                                                                          | <span data-ttu-id="476b2-109">衍生自</span><span class="sxs-lookup"><span data-stu-id="476b2-109">Derived from</span></span>                                                     | <span data-ttu-id="476b2-110">Description</span><span class="sxs-lookup"><span data-stu-id="476b2-110">Description</span></span>                                                                                                |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="476b2-111">**MonthlyDayOfWeekScheduleType) 的月份 (**</span><span class="sxs-lookup"><span data-stu-id="476b2-111">**Months (monthlyDayOfWeekScheduleType)**</span></span>](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="476b2-112">**monthsType**</span><span class="sxs-lookup"><span data-stu-id="476b2-112">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="476b2-113">指定在一年中的幾個月，工作會在一年中執行一周的每月日排程。</span><span class="sxs-lookup"><span data-stu-id="476b2-113">Specifies the months of the year during which the task runs for a monthly day-of-week schedule.</span></span><br/> |
| [<span data-ttu-id="476b2-114">**MonthlyScheduleType) 的月份 (**</span><span class="sxs-lookup"><span data-stu-id="476b2-114">**Months (monthlyScheduleType)**</span></span>](taskschedulerschema-months-monthlyscheduletype-element.md)                   | [<span data-ttu-id="476b2-115">**monthsType**</span><span class="sxs-lookup"><span data-stu-id="476b2-115">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="476b2-116">指定執行每月排程之工作的年度月份。</span><span class="sxs-lookup"><span data-stu-id="476b2-116">Specifies the months of the year during which the task runs for a monthly schedule.</span></span><br/>             |



## <a name="examples"></a><span data-ttu-id="476b2-117">範例</span><span class="sxs-lookup"><span data-stu-id="476b2-117">Examples</span></span>

<span data-ttu-id="476b2-118">下列 XML 定義在六月執行工作的月份行事曆。</span><span class="sxs-lookup"><span data-stu-id="476b2-118">The following XML defines a months calendar that runs the task in June.</span></span>


```XML
<Months>
    <June/>
</Months>
```



## <a name="requirements"></a><span data-ttu-id="476b2-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="476b2-119">Requirements</span></span>



| <span data-ttu-id="476b2-120">需求</span><span class="sxs-lookup"><span data-stu-id="476b2-120">Requirement</span></span> | <span data-ttu-id="476b2-121">值</span><span class="sxs-lookup"><span data-stu-id="476b2-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="476b2-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="476b2-122">Minimum supported client</span></span><br/> | <span data-ttu-id="476b2-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="476b2-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="476b2-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="476b2-124">Minimum supported server</span></span><br/> | <span data-ttu-id="476b2-125">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="476b2-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="476b2-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="476b2-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="476b2-127">工作排程器架構元素</span><span class="sxs-lookup"><span data-stu-id="476b2-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="476b2-128">工作排程器</span><span class="sxs-lookup"><span data-stu-id="476b2-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





