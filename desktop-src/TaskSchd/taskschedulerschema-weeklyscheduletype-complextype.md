---
title: weeklyScheduleType 複雜類型
description: 定義 ScheduleByWeek 元素的子項目和排序資訊。
ms.assetid: 048832fa-2262-4461-9cfc-823a4eb7a1df
keywords:
- weeklyScheduleType 複雜類型工作排程器
topic_type:
- apiref
api_name:
- weeklyScheduleType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 797e01c20e749593d64bad12f017af8be613992e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384349"
---
# <a name="weeklyscheduletype-complex-type"></a><span data-ttu-id="bade9-104">weeklyScheduleType 複雜類型</span><span class="sxs-lookup"><span data-stu-id="bade9-104">weeklyScheduleType Complex Type</span></span>

<span data-ttu-id="bade9-105">定義 [**ScheduleByWeek**](taskschedulerschema-schedulebyweek-calendartriggertype-element.md) 元素的子項目和排序資訊。</span><span class="sxs-lookup"><span data-stu-id="bade9-105">Defines the child elements and sequencing information for the [**ScheduleByWeek**](taskschedulerschema-schedulebyweek-calendartriggertype-element.md) element.</span></span>

``` syntax
<xs:complexType name="weeklyScheduleType">
    <xs:all>
        <xs:element name="WeeksInterval"
            minOccurs="0"
        >
            <xs:simpleType>
                <xs:restriction
                    base="unsignedByte"
                >
                    <xs:minInclusive
                        value="1"
                     />
                    <xs:maxInclusive
                        value="52"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
        <xs:element name="DaysOfWeek"
            type="daysOfWeekType"
            minOccurs="0"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="bade9-106">子元素</span><span class="sxs-lookup"><span data-stu-id="bade9-106">Child elements</span></span>



| <span data-ttu-id="bade9-107">元素</span><span class="sxs-lookup"><span data-stu-id="bade9-107">Element</span></span>                                                                               | <span data-ttu-id="bade9-108">類型</span><span class="sxs-lookup"><span data-stu-id="bade9-108">Type</span></span>                                                                     | <span data-ttu-id="bade9-109">Description</span><span class="sxs-lookup"><span data-stu-id="bade9-109">Description</span></span>                                                          |
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="bade9-110">**DaysOfWeek**</span><span class="sxs-lookup"><span data-stu-id="bade9-110">**DaysOfWeek**</span></span>](taskschedulerschema-daysofweek-weeklyscheduletype-element.md)       | [<span data-ttu-id="bade9-111">**daysOfWeekType**</span><span class="sxs-lookup"><span data-stu-id="bade9-111">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md) | <span data-ttu-id="bade9-112">指定工作執行的星期幾。</span><span class="sxs-lookup"><span data-stu-id="bade9-112">Specifies the days of the week in which the task runs.</span></span><br/>    |
| [<span data-ttu-id="bade9-113">**WeeksInterval**</span><span class="sxs-lookup"><span data-stu-id="bade9-113">**WeeksInterval**</span></span>](taskschedulerschema-weeksinterval-weeklyscheduletype-element.md) |                                                                          | <span data-ttu-id="bade9-114">指定排程中周之間的間隔。</span><span class="sxs-lookup"><span data-stu-id="bade9-114">Specifies the interval between the weeks in the schedule.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="bade9-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="bade9-115">Requirements</span></span>



| <span data-ttu-id="bade9-116">需求</span><span class="sxs-lookup"><span data-stu-id="bade9-116">Requirement</span></span> | <span data-ttu-id="bade9-117">值</span><span class="sxs-lookup"><span data-stu-id="bade9-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="bade9-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bade9-118">Minimum supported client</span></span><br/> | <span data-ttu-id="bade9-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bade9-119">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="bade9-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bade9-120">Minimum supported server</span></span><br/> | <span data-ttu-id="bade9-121">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bade9-121">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bade9-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bade9-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bade9-123">工作排程器</span><span class="sxs-lookup"><span data-stu-id="bade9-123">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





