---
title: dailyScheduleType 複雜類型
description: 定義 ScheduleByDay 元素的子項目和排序資訊。
ms.assetid: e0b1b09f-d72a-4a85-9059-4a917bc0104a
keywords:
- dailyScheduleType 複雜類型工作排程器
topic_type:
- apiref
api_name:
- dailyScheduleType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5982ab7e72a79dc909a4e91fafe363ca4703639d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106990910"
---
# <a name="dailyscheduletype-complex-type"></a><span data-ttu-id="ebe8c-104">dailyScheduleType 複雜類型</span><span class="sxs-lookup"><span data-stu-id="ebe8c-104">dailyScheduleType Complex Type</span></span>

<span data-ttu-id="ebe8c-105">定義 [**ScheduleByDay**](taskschedulerschema-schedulebyday-calendartriggertype-element.md) 元素的子項目和排序資訊。</span><span class="sxs-lookup"><span data-stu-id="ebe8c-105">Defines the child elements and sequencing information for the [**ScheduleByDay**](taskschedulerschema-schedulebyday-calendartriggertype-element.md) element.</span></span>

``` syntax
<xs:complexType name="dailyScheduleType">
    <xs:all>
        <xs:element name="DaysInterval"
            minOccurs="0"
        >
            <xs:simpleType>
                <xs:restriction
                    base="unsignedInt"
                >
                    <xs:minInclusive
                        value="1"
                     />
                    <xs:maxInclusive
                        value="365"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="ebe8c-106">子元素</span><span class="sxs-lookup"><span data-stu-id="ebe8c-106">Child elements</span></span>



| <span data-ttu-id="ebe8c-107">元素</span><span class="sxs-lookup"><span data-stu-id="ebe8c-107">Element</span></span>                                                                            | <span data-ttu-id="ebe8c-108">類型</span><span class="sxs-lookup"><span data-stu-id="ebe8c-108">Type</span></span> | <span data-ttu-id="ebe8c-109">Description</span><span class="sxs-lookup"><span data-stu-id="ebe8c-109">Description</span></span>                                                          |
|------------------------------------------------------------------------------------|------|----------------------------------------------------------------------|
| [<span data-ttu-id="ebe8c-110">**DaysInterval**</span><span class="sxs-lookup"><span data-stu-id="ebe8c-110">**DaysInterval**</span></span>](taskschedulerschema-daysinterval-dailyscheduletype-element.md) |      | <span data-ttu-id="ebe8c-111">指定排程中天數之間的間隔。</span><span class="sxs-lookup"><span data-stu-id="ebe8c-111">Specifies the interval between the days in the schedule.</span></span> <br/> |



## <a name="requirements"></a><span data-ttu-id="ebe8c-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="ebe8c-112">Requirements</span></span>



| <span data-ttu-id="ebe8c-113">需求</span><span class="sxs-lookup"><span data-stu-id="ebe8c-113">Requirement</span></span> | <span data-ttu-id="ebe8c-114">值</span><span class="sxs-lookup"><span data-stu-id="ebe8c-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ebe8c-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ebe8c-115">Minimum supported client</span></span><br/> | <span data-ttu-id="ebe8c-116">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ebe8c-116">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ebe8c-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ebe8c-117">Minimum supported server</span></span><br/> | <span data-ttu-id="ebe8c-118">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ebe8c-118">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ebe8c-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ebe8c-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebe8c-120">工作排程器架構複雜類型</span><span class="sxs-lookup"><span data-stu-id="ebe8c-120">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="ebe8c-121">工作排程器</span><span class="sxs-lookup"><span data-stu-id="ebe8c-121">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





