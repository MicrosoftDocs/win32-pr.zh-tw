---
title: timeTriggerType 複雜類型
description: 定義 TimeTrigger 元素的基底類型。
ms.assetid: 3aabfb7a-3e11-4b67-8345-cc5088f11efc
keywords:
- timeTriggerType 複雜類型工作排程器
topic_type:
- apiref
api_name:
- timeTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6f44f0959a9f67e4bfee0b0ef5dd7f095ffbadce
ms.sourcegitcommit: b3a9abea47dea7374eac0f9a95a652ac6977fb2e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/20/2021
ms.locfileid: "107734133"
---
# <a name="timetriggertype-complex-type"></a><span data-ttu-id="9317d-104">timeTriggerType 複雜類型</span><span class="sxs-lookup"><span data-stu-id="9317d-104">timeTriggerType Complex Type</span></span>

<span data-ttu-id="9317d-105">定義 [**TimeTrigger**](taskschedulerschema-timetrigger-triggergroup-element.md) 元素的基底類型。</span><span class="sxs-lookup"><span data-stu-id="9317d-105">Defines the base type for the [**TimeTrigger**](taskschedulerschema-timetrigger-triggergroup-element.md) element.</span></span>

``` syntax
<xs:complexType name="timeTriggerType">
    <xs:complexContent>
        <xs:extension
            base="triggerBaseType"
        >
            <xs:sequence>
                <xs:element name="RandomDelay"
                    type="duration"
                    default="PT0M"
                 />
            </xs:sequence>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="9317d-106">子元素</span><span class="sxs-lookup"><span data-stu-id="9317d-106">Child elements</span></span>



| <span data-ttu-id="9317d-107">元素</span><span class="sxs-lookup"><span data-stu-id="9317d-107">Element</span></span>                                                                        | <span data-ttu-id="9317d-108">類型</span><span class="sxs-lookup"><span data-stu-id="9317d-108">Type</span></span>     | <span data-ttu-id="9317d-109">Description</span><span class="sxs-lookup"><span data-stu-id="9317d-109">Description</span></span>                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9317d-110">**RandomDelay**</span><span class="sxs-lookup"><span data-stu-id="9317d-110">**RandomDelay**</span></span>](taskschedulerschema-randomdelay-timetriggertype-element.md) | <span data-ttu-id="9317d-111">duration</span><span class="sxs-lookup"><span data-stu-id="9317d-111">duration</span></span> | <span data-ttu-id="9317d-112">指定隨機新增至觸發程式開始時間的延遲時間。</span><span class="sxs-lookup"><span data-stu-id="9317d-112">Specifies the delay time that is randomly added to the start time of the trigger.</span></span> <span data-ttu-id="9317d-113">此字串的格式為 `P<days>DT<hours>H<minutes>M<seconds>S` (例如，P2DT5S 是2天、5秒的延遲) 。</span><span class="sxs-lookup"><span data-stu-id="9317d-113">The format for this string is `P<days>DT<hours>H<minutes>M<seconds>S` (for example, P2DT5S is a 2 day, 5 second delay).</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="9317d-114">備註</span><span class="sxs-lookup"><span data-stu-id="9317d-114">Remarks</span></span>

<span data-ttu-id="9317d-115">請注意，此元素不會將任何子項目加入至 [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) 複雜型別所定義的專案。</span><span class="sxs-lookup"><span data-stu-id="9317d-115">Note that this element does not add any child elements to those defined by the [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="9317d-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="9317d-116">Requirements</span></span>



| <span data-ttu-id="9317d-117">需求</span><span class="sxs-lookup"><span data-stu-id="9317d-117">Requirement</span></span> | <span data-ttu-id="9317d-118">值</span><span class="sxs-lookup"><span data-stu-id="9317d-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9317d-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9317d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="9317d-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9317d-120">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="9317d-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9317d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="9317d-122">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9317d-122">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9317d-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9317d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9317d-124">工作排程器架構複雜類型</span><span class="sxs-lookup"><span data-stu-id="9317d-124">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="9317d-125">工作排程器</span><span class="sxs-lookup"><span data-stu-id="9317d-125">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





