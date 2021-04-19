---
title: WeeksType) 元素 (周
description: 指定當月的特定周。
ms.assetid: 0cec07da-e9e7-43ef-9f54-48d00114ba1f
keywords:
- Week 元素工作排程器
topic_type:
- apiref
api_name:
- Week
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0487aa07e1f1132c998b6cb2ba0f518a9db57ce2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106970452"
---
# <a name="week-weekstype-element"></a><span data-ttu-id="305a5-104">WeeksType) 元素 (周</span><span class="sxs-lookup"><span data-stu-id="305a5-104">Week (weeksType) Element</span></span>

<span data-ttu-id="305a5-105">指定當月的特定周。</span><span class="sxs-lookup"><span data-stu-id="305a5-105">Specifies a specific week of the month.</span></span>

``` syntax
<xs:element name="Week"
    type="weekType"
 />
```

<span data-ttu-id="305a5-106">Week 元素是由 [**weeksType**](taskschedulerschema-weekstype-complextype.md)複雜型 **別** 定義。</span><span class="sxs-lookup"><span data-stu-id="305a5-106">The **Week** element is defined by the [**weeksType**](taskschedulerschema-weekstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="305a5-107">父元素</span><span class="sxs-lookup"><span data-stu-id="305a5-107">Parent element</span></span>



| <span data-ttu-id="305a5-108">元素</span><span class="sxs-lookup"><span data-stu-id="305a5-108">Element</span></span>                                                                                                        | <span data-ttu-id="305a5-109">衍生自</span><span class="sxs-lookup"><span data-stu-id="305a5-109">Derived from</span></span>                                                   | <span data-ttu-id="305a5-110">Description</span><span class="sxs-lookup"><span data-stu-id="305a5-110">Description</span></span>                                                           |
|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="305a5-111">**MonthlyDayOfWeekScheduleType)  (周**</span><span class="sxs-lookup"><span data-stu-id="305a5-111">**Weeks (monthlyDayOfWeekScheduleType)**</span></span>](taskschedulerschema-weeks-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="305a5-112">**weeksType**</span><span class="sxs-lookup"><span data-stu-id="305a5-112">**weeksType**</span></span>](taskschedulerschema-weekstype-complextype.md) | <span data-ttu-id="305a5-113">指定執行工作的月份周數。</span><span class="sxs-lookup"><span data-stu-id="305a5-113">Specifies the weeks of the month in which the task is run.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="305a5-114">備註</span><span class="sxs-lookup"><span data-stu-id="305a5-114">Remarks</span></span>

<span data-ttu-id="305a5-115">指定月中的周數時，請在當月的前四個星期使用數位1-4，或使用 "Last" 字串來指出當月的最後一周。</span><span class="sxs-lookup"><span data-stu-id="305a5-115">When specifying the weeks of the month, use the numbers 1-4 for the first four weeks of the month or use the string "Last" to indicate that last week of the month.</span></span>

## <a name="requirements"></a><span data-ttu-id="305a5-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="305a5-116">Requirements</span></span>



| <span data-ttu-id="305a5-117">需求</span><span class="sxs-lookup"><span data-stu-id="305a5-117">Requirement</span></span> | <span data-ttu-id="305a5-118">值</span><span class="sxs-lookup"><span data-stu-id="305a5-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="305a5-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="305a5-119">Minimum supported client</span></span><br/> | <span data-ttu-id="305a5-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="305a5-120">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="305a5-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="305a5-121">Minimum supported server</span></span><br/> | <span data-ttu-id="305a5-122">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="305a5-122">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="305a5-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="305a5-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="305a5-124">工作排程器架構元素</span><span class="sxs-lookup"><span data-stu-id="305a5-124">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="305a5-125">工作排程器</span><span class="sxs-lookup"><span data-stu-id="305a5-125">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





