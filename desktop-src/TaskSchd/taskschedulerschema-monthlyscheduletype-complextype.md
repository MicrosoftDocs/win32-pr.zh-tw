---
title: monthlyScheduleType 複雜類型
description: 定義 ScheduleByMonth (calendarTriggerType) 元素的子項目和排序資訊。
ms.assetid: 3ade775c-ca44-403e-9602-80095c7dba1a
keywords:
- monthlyScheduleType 複雜類型工作排程器
topic_type:
- apiref
api_name:
- monthlyScheduleType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 132c2fafe2b05a01380c13aae2ab7cb3ddaa5330
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966496"
---
# <a name="monthlyscheduletype-complex-type"></a><span data-ttu-id="12652-104">monthlyScheduleType 複雜類型</span><span class="sxs-lookup"><span data-stu-id="12652-104">monthlyScheduleType Complex Type</span></span>

<span data-ttu-id="12652-105">定義 [**ScheduleByMonth (calendarTriggerType)**](taskschedulerschema-schedulebymonth-calendartriggertype-element.md) 元素的子項目和排序資訊。</span><span class="sxs-lookup"><span data-stu-id="12652-105">Defines the child elements and sequencing information for the [**ScheduleByMonth (calendarTriggerType)**](taskschedulerschema-schedulebymonth-calendartriggertype-element.md) element.</span></span>

``` syntax
<xs:complexType name="monthlyScheduleType">
    <xs:all>
        <xs:element name="DaysOfMonth"
            type="daysOfMonthType"
            minOccurs="0"
         />
        <xs:element name="Months"
            type="monthsType"
            minOccurs="0"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="12652-106">子元素</span><span class="sxs-lookup"><span data-stu-id="12652-106">Child elements</span></span>



| <span data-ttu-id="12652-107">元素</span><span class="sxs-lookup"><span data-stu-id="12652-107">Element</span></span>                                                                            | <span data-ttu-id="12652-108">類型</span><span class="sxs-lookup"><span data-stu-id="12652-108">Type</span></span>                                                                       | <span data-ttu-id="12652-109">Description</span><span class="sxs-lookup"><span data-stu-id="12652-109">Description</span></span>                                                                                    |
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="12652-110">**DaysOfMonth**</span><span class="sxs-lookup"><span data-stu-id="12652-110">**DaysOfMonth**</span></span>](taskschedulerschema-daysofmonth-monthlyscheduletype-element.md) | [<span data-ttu-id="12652-111">**daysOfMonthType**</span><span class="sxs-lookup"><span data-stu-id="12652-111">**daysOfMonthType**</span></span>](taskschedulerschema-daysofmonthtype-complextype.md) | <span data-ttu-id="12652-112">指定工作執行的當月天數。</span><span class="sxs-lookup"><span data-stu-id="12652-112">Specifies the days of the month during which the task runs.</span></span><br/>                         |
| [<span data-ttu-id="12652-113">**月**</span><span class="sxs-lookup"><span data-stu-id="12652-113">**Months**</span></span>](taskschedulerschema-months-monthlyscheduletype-element.md)           | [<span data-ttu-id="12652-114">**monthsType**</span><span class="sxs-lookup"><span data-stu-id="12652-114">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md)           | <span data-ttu-id="12652-115">指定執行每月排程之工作的年度月份。</span><span class="sxs-lookup"><span data-stu-id="12652-115">Specifies the months of the year during which the task runs for a monthly schedule.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="12652-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="12652-116">Requirements</span></span>



| <span data-ttu-id="12652-117">需求</span><span class="sxs-lookup"><span data-stu-id="12652-117">Requirement</span></span> | <span data-ttu-id="12652-118">值</span><span class="sxs-lookup"><span data-stu-id="12652-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="12652-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="12652-119">Minimum supported client</span></span><br/> | <span data-ttu-id="12652-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="12652-120">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="12652-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="12652-121">Minimum supported server</span></span><br/> | <span data-ttu-id="12652-122">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="12652-122">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="12652-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="12652-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12652-124">工作排程器架構複雜類型</span><span class="sxs-lookup"><span data-stu-id="12652-124">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="12652-125">工作排程器</span><span class="sxs-lookup"><span data-stu-id="12652-125">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





