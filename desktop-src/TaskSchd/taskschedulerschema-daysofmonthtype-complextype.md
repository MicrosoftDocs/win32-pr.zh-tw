---
title: daysOfMonthType 複雜類型
description: 定義 DaysOfMonth (monthlyScheduleType) 元素的子項目和排序資訊。
ms.assetid: 8258c090-c836-497e-8e5b-db4782277822
keywords:
- daysOfMonthType 複雜類型工作排程器
topic_type:
- apiref
api_name:
- daysOfMonthType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f1459528b47bf01a9e336b758b739c3f5751ee1c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385073"
---
# <a name="daysofmonthtype-complex-type"></a><span data-ttu-id="ed2d1-104">daysOfMonthType 複雜類型</span><span class="sxs-lookup"><span data-stu-id="ed2d1-104">daysOfMonthType Complex Type</span></span>

<span data-ttu-id="ed2d1-105">定義 [**DaysOfMonth (monthlyScheduleType)**](taskschedulerschema-daysofmonth-monthlyscheduletype-element.md) 元素的子項目和排序資訊。</span><span class="sxs-lookup"><span data-stu-id="ed2d1-105">Defines the child element and sequencing information for the [**DaysOfMonth (monthlyScheduleType)**](taskschedulerschema-daysofmonth-monthlyscheduletype-element.md) element.</span></span>

``` syntax
<xs:complexType name="daysOfMonthType">
    <xs:sequence>
        <xs:element name="Day"
            type="dayOfMonthType"
            minOccurs="0"
            maxOccurs="32"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="ed2d1-106">子元素</span><span class="sxs-lookup"><span data-stu-id="ed2d1-106">Child elements</span></span>



| <span data-ttu-id="ed2d1-107">元素</span><span class="sxs-lookup"><span data-stu-id="ed2d1-107">Element</span></span>                                                        | <span data-ttu-id="ed2d1-108">類型</span><span class="sxs-lookup"><span data-stu-id="ed2d1-108">Type</span></span>                                                                    | <span data-ttu-id="ed2d1-109">Description</span><span class="sxs-lookup"><span data-stu-id="ed2d1-109">Description</span></span>                                                          |
|----------------------------------------------------------------|-------------------------------------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="ed2d1-110">**天**</span><span class="sxs-lookup"><span data-stu-id="ed2d1-110">**Day**</span></span>](taskschedulerschema-day-daysofmonthtype-element.md) | [<span data-ttu-id="ed2d1-111">**dayOfMonthType**</span><span class="sxs-lookup"><span data-stu-id="ed2d1-111">**dayOfMonthType**</span></span>](taskschedulerschema-dayofmonthtype-simpletype.md) | <span data-ttu-id="ed2d1-112">指定執行工作的月份日期。</span><span class="sxs-lookup"><span data-stu-id="ed2d1-112">Specifies a day of the month during which the task runs.</span></span> <br/> |



## <a name="requirements"></a><span data-ttu-id="ed2d1-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="ed2d1-113">Requirements</span></span>



| <span data-ttu-id="ed2d1-114">需求</span><span class="sxs-lookup"><span data-stu-id="ed2d1-114">Requirement</span></span> | <span data-ttu-id="ed2d1-115">值</span><span class="sxs-lookup"><span data-stu-id="ed2d1-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ed2d1-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ed2d1-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ed2d1-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ed2d1-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ed2d1-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ed2d1-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ed2d1-119">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ed2d1-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ed2d1-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ed2d1-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed2d1-121">工作排程器架構複雜類型</span><span class="sxs-lookup"><span data-stu-id="ed2d1-121">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="ed2d1-122">工作排程器</span><span class="sxs-lookup"><span data-stu-id="ed2d1-122">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





