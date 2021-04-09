---
title: monthsType 複雜類型
description: 定義專案的子專案和排序資訊 (monthlyDayOfWeekScheduleType) 和月份 (monthlyScheduleType) 元素。
ms.assetid: f1faa67a-2f5f-4a00-a1df-2d44e218278b
keywords:
- monthsType 複雜類型工作排程器
topic_type:
- apiref
api_name:
- monthsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e6a19000073fd12e05aa915921850264979a0541
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685642"
---
# <a name="monthstype-complex-type"></a><span data-ttu-id="89a62-104">monthsType 複雜類型</span><span class="sxs-lookup"><span data-stu-id="89a62-104">monthsType Complex Type</span></span>

<span data-ttu-id="89a62-105">定義專案的子專案和排序資訊 [**(monthlyDayOfWeekScheduleType)**](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) 和 [**月份 (monthlyScheduleType)**](taskschedulerschema-months-monthlyscheduletype-element.md) 元素。</span><span class="sxs-lookup"><span data-stu-id="89a62-105">Defines the child elements and sequencing information for the [**Months (monthlyDayOfWeekScheduleType)**](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) and [**Months (monthlyScheduleType)**](taskschedulerschema-months-monthlyscheduletype-element.md) elements.</span></span>

``` syntax
<xs:complexType name="monthsType">
    <xs:all>
        <xs:element name="January"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="February"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="March"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="April"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="May"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="June"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="July"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="August"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="September"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="October"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="November"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="December"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="89a62-106">子元素</span><span class="sxs-lookup"><span data-stu-id="89a62-106">Child elements</span></span>



| <span data-ttu-id="89a62-107">元素</span><span class="sxs-lookup"><span data-stu-id="89a62-107">Element</span></span>                                                               | <span data-ttu-id="89a62-108">類型</span><span class="sxs-lookup"><span data-stu-id="89a62-108">Type</span></span> | <span data-ttu-id="89a62-109">Description</span><span class="sxs-lookup"><span data-stu-id="89a62-109">Description</span></span>                                            |
|-----------------------------------------------------------------------|------|--------------------------------------------------------|
| [<span data-ttu-id="89a62-110">**4 月**</span><span class="sxs-lookup"><span data-stu-id="89a62-110">**April**</span></span>](taskschedulerschema-april-monthstype-element.md)         | <span data-ttu-id="89a62-111">N/A</span><span class="sxs-lookup"><span data-stu-id="89a62-111">N/A</span></span>  | <span data-ttu-id="89a62-112">指定工作會在四月執行。</span><span class="sxs-lookup"><span data-stu-id="89a62-112">Specifies that the task runs in April.</span></span> <br/>     |
| [<span data-ttu-id="89a62-113">**8 月**</span><span class="sxs-lookup"><span data-stu-id="89a62-113">**August**</span></span>](taskschedulerschema-august-monthstype-element.md)       | <span data-ttu-id="89a62-114">N/A</span><span class="sxs-lookup"><span data-stu-id="89a62-114">N/A</span></span>  | <span data-ttu-id="89a62-115">指定工作在8月執行。</span><span class="sxs-lookup"><span data-stu-id="89a62-115">Specifies that the task runs in August.</span></span> <br/>    |
| [<span data-ttu-id="89a62-116">**12 月**</span><span class="sxs-lookup"><span data-stu-id="89a62-116">**December**</span></span>](taskschedulerschema-december-monthstype-element.md)   | <span data-ttu-id="89a62-117">N/A</span><span class="sxs-lookup"><span data-stu-id="89a62-117">N/A</span></span>  | <span data-ttu-id="89a62-118">指定工作會在十二月執行。</span><span class="sxs-lookup"><span data-stu-id="89a62-118">Specifies that the task runs in December.</span></span> <br/>  |
| [<span data-ttu-id="89a62-119">**2 月**</span><span class="sxs-lookup"><span data-stu-id="89a62-119">**February**</span></span>](taskschedulerschema-february-monthstype-element.md)   | <span data-ttu-id="89a62-120">N/A</span><span class="sxs-lookup"><span data-stu-id="89a62-120">N/A</span></span>  | <span data-ttu-id="89a62-121">指定工作會在二月執行。</span><span class="sxs-lookup"><span data-stu-id="89a62-121">Specifies that the task runs in February.</span></span> <br/>  |
| [<span data-ttu-id="89a62-122">**1 月**</span><span class="sxs-lookup"><span data-stu-id="89a62-122">**January**</span></span>](taskschedulerschema-january-monthstype-element.md)     | <span data-ttu-id="89a62-123">N/A</span><span class="sxs-lookup"><span data-stu-id="89a62-123">N/A</span></span>  | <span data-ttu-id="89a62-124">指定工作會在一月執行。</span><span class="sxs-lookup"><span data-stu-id="89a62-124">Specifies that the task runs in January.</span></span> <br/>   |
| [<span data-ttu-id="89a62-125">**7 月**</span><span class="sxs-lookup"><span data-stu-id="89a62-125">**July**</span></span>](taskschedulerschema-july-monthstype-element.md)           | <span data-ttu-id="89a62-126">N/A</span><span class="sxs-lookup"><span data-stu-id="89a62-126">N/A</span></span>  | <span data-ttu-id="89a62-127">指定工作會在七月執行。</span><span class="sxs-lookup"><span data-stu-id="89a62-127">Specifies that the task runs in July.</span></span> <br/>      |
| [<span data-ttu-id="89a62-128">**6 月**</span><span class="sxs-lookup"><span data-stu-id="89a62-128">**June**</span></span>](taskschedulerschema-june-monthstype-element.md)           | <span data-ttu-id="89a62-129">N/A</span><span class="sxs-lookup"><span data-stu-id="89a62-129">N/A</span></span>  | <span data-ttu-id="89a62-130">指定工作在六月執行。</span><span class="sxs-lookup"><span data-stu-id="89a62-130">Specifies that the task runs in June.</span></span> <br/>      |
| [<span data-ttu-id="89a62-131">**3 月**</span><span class="sxs-lookup"><span data-stu-id="89a62-131">**March**</span></span>](taskschedulerschema-march-monthstype-element.md)         | <span data-ttu-id="89a62-132">N/A</span><span class="sxs-lookup"><span data-stu-id="89a62-132">N/A</span></span>  | <span data-ttu-id="89a62-133">指定工作在三月執行。</span><span class="sxs-lookup"><span data-stu-id="89a62-133">Specifies that the task runs in March.</span></span> <br/>     |
| [<span data-ttu-id="89a62-134">**五月**</span><span class="sxs-lookup"><span data-stu-id="89a62-134">**May**</span></span>](taskschedulerschema-may-monthstype-element.md)             | <span data-ttu-id="89a62-135">N/A</span><span class="sxs-lookup"><span data-stu-id="89a62-135">N/A</span></span>  | <span data-ttu-id="89a62-136">指定工作在5月執行。</span><span class="sxs-lookup"><span data-stu-id="89a62-136">Specifies that the task runs in May.</span></span> <br/>       |
| [<span data-ttu-id="89a62-137">**11 月**</span><span class="sxs-lookup"><span data-stu-id="89a62-137">**November**</span></span>](taskschedulerschema-november-monthstype-element.md)   | <span data-ttu-id="89a62-138">N/A</span><span class="sxs-lookup"><span data-stu-id="89a62-138">N/A</span></span>  | <span data-ttu-id="89a62-139">指定工作在11月執行。</span><span class="sxs-lookup"><span data-stu-id="89a62-139">Specifies that the task runs in November.</span></span> <br/>  |
| [<span data-ttu-id="89a62-140">**10 月**</span><span class="sxs-lookup"><span data-stu-id="89a62-140">**October**</span></span>](taskschedulerschema-october-monthstype-element.md)     | <span data-ttu-id="89a62-141">N/A</span><span class="sxs-lookup"><span data-stu-id="89a62-141">N/A</span></span>  | <span data-ttu-id="89a62-142">指定工作在十月執行。</span><span class="sxs-lookup"><span data-stu-id="89a62-142">Specifies that the task runs in October.</span></span> <br/>   |
| [<span data-ttu-id="89a62-143">**9 月**</span><span class="sxs-lookup"><span data-stu-id="89a62-143">**September**</span></span>](taskschedulerschema-september-monthstype-element.md) | <span data-ttu-id="89a62-144">N/A</span><span class="sxs-lookup"><span data-stu-id="89a62-144">N/A</span></span>  | <span data-ttu-id="89a62-145">指定工作在九月執行。</span><span class="sxs-lookup"><span data-stu-id="89a62-145">Specifies that the task runs in September.</span></span> <br/> |



## <a name="requirements"></a><span data-ttu-id="89a62-146">規格需求</span><span class="sxs-lookup"><span data-stu-id="89a62-146">Requirements</span></span>



| <span data-ttu-id="89a62-147">需求</span><span class="sxs-lookup"><span data-stu-id="89a62-147">Requirement</span></span> | <span data-ttu-id="89a62-148">值</span><span class="sxs-lookup"><span data-stu-id="89a62-148">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="89a62-149">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="89a62-149">Minimum supported client</span></span><br/> | <span data-ttu-id="89a62-150">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="89a62-150">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="89a62-151">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="89a62-151">Minimum supported server</span></span><br/> | <span data-ttu-id="89a62-152">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="89a62-152">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="89a62-153">另請參閱</span><span class="sxs-lookup"><span data-stu-id="89a62-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89a62-154">工作排程器架構複雜類型</span><span class="sxs-lookup"><span data-stu-id="89a62-154">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="89a62-155">工作排程器</span><span class="sxs-lookup"><span data-stu-id="89a62-155">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





