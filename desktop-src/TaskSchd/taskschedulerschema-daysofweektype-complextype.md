---
title: daysOfWeekType 複雜類型
description: 定義 DaysOfWeek (weeklyScheduleType) 和 DaysOfWeek (monthlyDayOfWeekScheduleType) 元素的子項目和排序資訊。
ms.assetid: b3315582-af7a-4d4c-8f6f-61de12a85f46
keywords:
- daysOfWeekType 複雜類型工作排程器
topic_type:
- apiref
api_name:
- daysOfWeekType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0b4a1b5e6aeaa77c0bdfe12b1d5b68fde018f236
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317511"
---
# <a name="daysofweektype-complex-type"></a><span data-ttu-id="7b81a-104">daysOfWeekType 複雜類型</span><span class="sxs-lookup"><span data-stu-id="7b81a-104">daysOfWeekType Complex Type</span></span>

<span data-ttu-id="7b81a-105">定義 [**DaysOfWeek (weeklyScheduleType)**](taskschedulerschema-daysofweek-weeklyscheduletype-element.md) 和 [**DaysOfWeek (monthlyDayOfWeekScheduleType)**](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) 元素的子項目和排序資訊。</span><span class="sxs-lookup"><span data-stu-id="7b81a-105">Defines the child elements and sequencing information for the [**DaysOfWeek (weeklyScheduleType)**](taskschedulerschema-daysofweek-weeklyscheduletype-element.md) and [**DaysOfWeek (monthlyDayOfWeekScheduleType)**](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) elements.</span></span>

``` syntax
<xs:complexType name="daysOfWeekType">
    <xs:all>
        <xs:element name="Monday"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="Tuesday"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="Wednesday"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="Thursday"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="Friday"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="Saturday"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="Sunday"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="7b81a-106">子元素</span><span class="sxs-lookup"><span data-stu-id="7b81a-106">Child elements</span></span>



| <span data-ttu-id="7b81a-107">元素</span><span class="sxs-lookup"><span data-stu-id="7b81a-107">Element</span></span>                                                                   | <span data-ttu-id="7b81a-108">類型</span><span class="sxs-lookup"><span data-stu-id="7b81a-108">Type</span></span> | <span data-ttu-id="7b81a-109">Description</span><span class="sxs-lookup"><span data-stu-id="7b81a-109">Description</span></span>                         |
|---------------------------------------------------------------------------|------|-------------------------------------|
| [<span data-ttu-id="7b81a-110">**星期五**</span><span class="sxs-lookup"><span data-stu-id="7b81a-110">**Friday**</span></span>](taskschedulerschema-friday-daysofweektype-element.md)       | <span data-ttu-id="7b81a-111">N/A</span><span class="sxs-lookup"><span data-stu-id="7b81a-111">N/A</span></span>  | <span data-ttu-id="7b81a-112">工作會在星期五執行。</span><span class="sxs-lookup"><span data-stu-id="7b81a-112">Task runs on Friday.</span></span> <br/>    |
| [<span data-ttu-id="7b81a-113">**星期一**</span><span class="sxs-lookup"><span data-stu-id="7b81a-113">**Monday**</span></span>](taskschedulerschema-monday-daysofweektype-element.md)       | <span data-ttu-id="7b81a-114">N/A</span><span class="sxs-lookup"><span data-stu-id="7b81a-114">N/A</span></span>  | <span data-ttu-id="7b81a-115">工作會在星期一執行。</span><span class="sxs-lookup"><span data-stu-id="7b81a-115">Task runs on Monday.</span></span><br/>     |
| [<span data-ttu-id="7b81a-116">**星期六**</span><span class="sxs-lookup"><span data-stu-id="7b81a-116">**Saturday**</span></span>](taskschedulerschema-saturday-daysofweektype-element.md)   | <span data-ttu-id="7b81a-117">N/A</span><span class="sxs-lookup"><span data-stu-id="7b81a-117">N/A</span></span>  | <span data-ttu-id="7b81a-118">工作會在星期六執行。</span><span class="sxs-lookup"><span data-stu-id="7b81a-118">Task runs on Saturday.</span></span> <br/>  |
| [<span data-ttu-id="7b81a-119">**星期日**</span><span class="sxs-lookup"><span data-stu-id="7b81a-119">**Sunday**</span></span>](taskschedulerschema-sunday-daysofweektype-element.md)       | <span data-ttu-id="7b81a-120">N/A</span><span class="sxs-lookup"><span data-stu-id="7b81a-120">N/A</span></span>  | <span data-ttu-id="7b81a-121">工作會在星期日執行。</span><span class="sxs-lookup"><span data-stu-id="7b81a-121">Task runs on Sunday.</span></span> <br/>    |
| [<span data-ttu-id="7b81a-122">**Thursday**</span><span class="sxs-lookup"><span data-stu-id="7b81a-122">**Thursday**</span></span>](taskschedulerschema-thursday-daysofweektype-element.md)   | <span data-ttu-id="7b81a-123">N/A</span><span class="sxs-lookup"><span data-stu-id="7b81a-123">N/A</span></span>  | <span data-ttu-id="7b81a-124">工作在星期四執行</span><span class="sxs-lookup"><span data-stu-id="7b81a-124">Task runs on Thursday</span></span> <br/>   |
| [<span data-ttu-id="7b81a-125">**Tuesday**</span><span class="sxs-lookup"><span data-stu-id="7b81a-125">**Tuesday**</span></span>](taskschedulerschema-tuesday-daysofweektype-element.md)     | <span data-ttu-id="7b81a-126">N/A</span><span class="sxs-lookup"><span data-stu-id="7b81a-126">N/A</span></span>  | <span data-ttu-id="7b81a-127">工作會在星期二執行。</span><span class="sxs-lookup"><span data-stu-id="7b81a-127">Task runs on Tuesday.</span></span> <br/>   |
| [<span data-ttu-id="7b81a-128">**星期三**</span><span class="sxs-lookup"><span data-stu-id="7b81a-128">**Wednesday**</span></span>](taskschedulerschema-wednesday-daysofweektype-element.md) | <span data-ttu-id="7b81a-129">N/A</span><span class="sxs-lookup"><span data-stu-id="7b81a-129">N/A</span></span>  | <span data-ttu-id="7b81a-130">工作會在星期三執行。</span><span class="sxs-lookup"><span data-stu-id="7b81a-130">Task runs on Wednesday.</span></span> <br/> |



## <a name="requirements"></a><span data-ttu-id="7b81a-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="7b81a-131">Requirements</span></span>



| <span data-ttu-id="7b81a-132">需求</span><span class="sxs-lookup"><span data-stu-id="7b81a-132">Requirement</span></span> | <span data-ttu-id="7b81a-133">值</span><span class="sxs-lookup"><span data-stu-id="7b81a-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7b81a-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7b81a-134">Minimum supported client</span></span><br/> | <span data-ttu-id="7b81a-135">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7b81a-135">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="7b81a-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7b81a-136">Minimum supported server</span></span><br/> | <span data-ttu-id="7b81a-137">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7b81a-137">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7b81a-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7b81a-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b81a-139">工作排程器架構複雜類型</span><span class="sxs-lookup"><span data-stu-id="7b81a-139">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="7b81a-140">工作排程器</span><span class="sxs-lookup"><span data-stu-id="7b81a-140">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





