---
title: MonthlyScheduleType) 元素 (月份
description: 指定執行每月排程之工作的年度月份。
ms.assetid: 71c9f7ac-01fc-4837-bccf-1869df2bc24e
keywords:
- Months 元素工作排程器
topic_type:
- apiref
api_name:
- Months
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0ed40fd2466f8962f839f39e7addd3b7e1bc33eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105371"
---
# <a name="months-monthlyscheduletype-element"></a><span data-ttu-id="d2507-104">MonthlyScheduleType) 元素 (月份</span><span class="sxs-lookup"><span data-stu-id="d2507-104">Months (monthlyScheduleType) Element</span></span>

<span data-ttu-id="d2507-105">指定執行每月排程之工作的年度月份。</span><span class="sxs-lookup"><span data-stu-id="d2507-105">Specifies the months of the year during which the task runs for a monthly schedule.</span></span>

``` syntax
<xs:element name="Months"
    type="monthsType"
 />
```

<span data-ttu-id="d2507-106">**Months** 元素是由 [**monthlyScheduleType**](taskschedulerschema-monthlyscheduletype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="d2507-106">The **Months** element is defined by the [**monthlyScheduleType**](taskschedulerschema-monthlyscheduletype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="d2507-107">父元素</span><span class="sxs-lookup"><span data-stu-id="d2507-107">Parent element</span></span>



| <span data-ttu-id="d2507-108">元素</span><span class="sxs-lookup"><span data-stu-id="d2507-108">Element</span></span>                                                                                    | <span data-ttu-id="d2507-109">衍生自</span><span class="sxs-lookup"><span data-stu-id="d2507-109">Derived from</span></span>                                                                       | <span data-ttu-id="d2507-110">Description</span><span class="sxs-lookup"><span data-stu-id="d2507-110">Description</span></span>                               |
|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|-------------------------------------------|
| [<span data-ttu-id="d2507-111">**ScheduleByMonth**</span><span class="sxs-lookup"><span data-stu-id="d2507-111">**ScheduleByMonth**</span></span>](taskschedulerschema-schedulebymonth-calendartriggertype-element.md) | [<span data-ttu-id="d2507-112">**monthlyScheduleType**</span><span class="sxs-lookup"><span data-stu-id="d2507-112">**monthlyScheduleType**</span></span>](taskschedulerschema-monthlyscheduletype-complextype.md) | <span data-ttu-id="d2507-113">指定每月排程。</span><span class="sxs-lookup"><span data-stu-id="d2507-113">Specifies a monthly schedule.</span></span> <br/> |



## <a name="child-elements"></a><span data-ttu-id="d2507-114">子元素</span><span class="sxs-lookup"><span data-stu-id="d2507-114">Child elements</span></span>



| <span data-ttu-id="d2507-115">元素</span><span class="sxs-lookup"><span data-stu-id="d2507-115">Element</span></span>                                                                            | <span data-ttu-id="d2507-116">類型</span><span class="sxs-lookup"><span data-stu-id="d2507-116">Type</span></span> | <span data-ttu-id="d2507-117">Description</span><span class="sxs-lookup"><span data-stu-id="d2507-117">Description</span></span>                                           |
|------------------------------------------------------------------------------------|------|-------------------------------------------------------|
| [<span data-ttu-id="d2507-118">**四月 (monthsType)**</span><span class="sxs-lookup"><span data-stu-id="d2507-118">**April (monthsType)**</span></span>](taskschedulerschema-april-monthstype-element.md)         |      | <span data-ttu-id="d2507-119">指定工作會在四月執行。</span><span class="sxs-lookup"><span data-stu-id="d2507-119">Specifies that the task runs in April.</span></span><br/>     |
| [<span data-ttu-id="d2507-120">**八月 (monthsType)**</span><span class="sxs-lookup"><span data-stu-id="d2507-120">**August (monthsType)**</span></span>](taskschedulerschema-august-monthstype-element.md)       |      | <span data-ttu-id="d2507-121">指定工作在8月執行。</span><span class="sxs-lookup"><span data-stu-id="d2507-121">Specifies that the task runs in August.</span></span><br/>    |
| [<span data-ttu-id="d2507-122">**12月 (monthsType)**</span><span class="sxs-lookup"><span data-stu-id="d2507-122">**December (monthsType)**</span></span>](taskschedulerschema-december-monthstype-element.md)   |      | <span data-ttu-id="d2507-123">指定工作會在十二月執行。</span><span class="sxs-lookup"><span data-stu-id="d2507-123">Specifies that the task runs in December.</span></span><br/>  |
| [<span data-ttu-id="d2507-124">**二月 (monthsType)**</span><span class="sxs-lookup"><span data-stu-id="d2507-124">**February (monthsType)**</span></span>](taskschedulerschema-february-monthstype-element.md)   |      | <span data-ttu-id="d2507-125">指定工作會在二月執行。</span><span class="sxs-lookup"><span data-stu-id="d2507-125">Specifies that the task runs in February.</span></span><br/>  |
| [<span data-ttu-id="d2507-126">**1月 (monthsType)**</span><span class="sxs-lookup"><span data-stu-id="d2507-126">**January (monthsType)**</span></span>](taskschedulerschema-january-monthstype-element.md)     |      | <span data-ttu-id="d2507-127">指定工作會在一月執行。</span><span class="sxs-lookup"><span data-stu-id="d2507-127">Specifies that the task runs in January.</span></span><br/>   |
| [<span data-ttu-id="d2507-128">**七月 (monthsType)**</span><span class="sxs-lookup"><span data-stu-id="d2507-128">**July (monthsType)**</span></span>](taskschedulerschema-july-monthstype-element.md)           |      | <span data-ttu-id="d2507-129">指定工作會在七月執行。</span><span class="sxs-lookup"><span data-stu-id="d2507-129">Specifies that the task runs in July.</span></span><br/>      |
| [<span data-ttu-id="d2507-130">**六月 (monthsType)**</span><span class="sxs-lookup"><span data-stu-id="d2507-130">**June (monthsType)**</span></span>](taskschedulerschema-june-monthstype-element.md)           |      | <span data-ttu-id="d2507-131">指定工作在六月執行。</span><span class="sxs-lookup"><span data-stu-id="d2507-131">Specifies that the task runs in June.</span></span><br/>      |
| [<span data-ttu-id="d2507-132">**三月 (monthsType)**</span><span class="sxs-lookup"><span data-stu-id="d2507-132">**March (monthsType)**</span></span>](taskschedulerschema-march-monthstype-element.md)         |      | <span data-ttu-id="d2507-133">指定工作在三月執行。</span><span class="sxs-lookup"><span data-stu-id="d2507-133">Specifies that the task runs in March.</span></span><br/>     |
| [<span data-ttu-id="d2507-134">**可能 (monthsType)**</span><span class="sxs-lookup"><span data-stu-id="d2507-134">**May (monthsType)**</span></span>](taskschedulerschema-may-monthstype-element.md)             |      | <span data-ttu-id="d2507-135">指定工作在5月執行。</span><span class="sxs-lookup"><span data-stu-id="d2507-135">Specifies that the task runs in May.</span></span><br/>       |
| [<span data-ttu-id="d2507-136">**11月 (monthsType)**</span><span class="sxs-lookup"><span data-stu-id="d2507-136">**November (monthsType)**</span></span>](taskschedulerschema-november-monthstype-element.md)   |      | <span data-ttu-id="d2507-137">指定工作在11月執行。</span><span class="sxs-lookup"><span data-stu-id="d2507-137">Specifies that the task runs in November.</span></span><br/>  |
| [<span data-ttu-id="d2507-138">**十月 (monthsType)**</span><span class="sxs-lookup"><span data-stu-id="d2507-138">**October (monthsType)**</span></span>](taskschedulerschema-october-monthstype-element.md)     |      | <span data-ttu-id="d2507-139">指定工作在十月執行。</span><span class="sxs-lookup"><span data-stu-id="d2507-139">Specifies that the task runs in October.</span></span><br/>   |
| [<span data-ttu-id="d2507-140">**MonthsType) 的九月 (**</span><span class="sxs-lookup"><span data-stu-id="d2507-140">**September (monthsType)**</span></span>](taskschedulerschema-september-monthstype-element.md) |      | <span data-ttu-id="d2507-141">指定工作在九月執行。</span><span class="sxs-lookup"><span data-stu-id="d2507-141">Specifies that the task runs in September.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="d2507-142">備註</span><span class="sxs-lookup"><span data-stu-id="d2507-142">Remarks</span></span>

<span data-ttu-id="d2507-143">針對腳本開發，會使用 [**MonthlyTrigger MonthsOfYear**](monthlytrigger-monthsofyear.md) 屬性指定排程的月份。</span><span class="sxs-lookup"><span data-stu-id="d2507-143">For script development, the months of the schedule are specified using the [**MonthlyTrigger.MonthsOfYear**](monthlytrigger-monthsofyear.md) property.</span></span>

<span data-ttu-id="d2507-144">針對 c + + 開發，會使用 [**IMonthlyTrigger：： MonthsOfYear**](/windows/desktop/api/taskschd/nf-taskschd-imonthlytrigger-get_monthsofyear) 屬性指定排程的月份。</span><span class="sxs-lookup"><span data-stu-id="d2507-144">For C++ development, the months of the schedule are specified using the [**IMonthlyTrigger::MonthsOfYear**](/windows/desktop/api/taskschd/nf-taskschd-imonthlytrigger-get_monthsofyear) property.</span></span>

## <a name="examples"></a><span data-ttu-id="d2507-145">範例</span><span class="sxs-lookup"><span data-stu-id="d2507-145">Examples</span></span>

<span data-ttu-id="d2507-146">下列 XML 會定義每月首次開始工作的月曆，並在每個月的第15天開始。</span><span class="sxs-lookup"><span data-stu-id="d2507-146">The following XML defines a monthly calendar that starts the task on the 1st and 15th day of every month of the year.</span></span>


```XML
</ScheduleByMonth>
    <DaysOfMonth>
        <Day>1</Day>
        <Day>15</Day>
    </DaysOfMonth
    <Months>
        <January/>
        <February/>
        <March/>
        <April/>
        <May/>
        <June/>
        <July/>
        <August/>
        <September/>
        <October/>
        <November/>
        <December/>
    <Months>
</ScheduleByMonth>
```



## <a name="requirements"></a><span data-ttu-id="d2507-147">規格需求</span><span class="sxs-lookup"><span data-stu-id="d2507-147">Requirements</span></span>



| <span data-ttu-id="d2507-148">需求</span><span class="sxs-lookup"><span data-stu-id="d2507-148">Requirement</span></span> | <span data-ttu-id="d2507-149">值</span><span class="sxs-lookup"><span data-stu-id="d2507-149">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d2507-150">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d2507-150">Minimum supported client</span></span><br/> | <span data-ttu-id="d2507-151">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d2507-151">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d2507-152">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d2507-152">Minimum supported server</span></span><br/> | <span data-ttu-id="d2507-153">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d2507-153">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d2507-154">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d2507-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2507-155">工作排程器架構元素</span><span class="sxs-lookup"><span data-stu-id="d2507-155">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="d2507-156">工作排程器</span><span class="sxs-lookup"><span data-stu-id="d2507-156">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





