---
title: eventTriggerType 複雜類型
description: 定義 EventTrigger 元素的子項目和排序資訊。
ms.assetid: c678af6f-bdfb-4c4d-85d7-2d93abfc2a7d
keywords:
- eventTriggerType 複雜類型工作排程器
topic_type:
- apiref
api_name:
- eventTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 16c3d4257d89ebb8d0efb6dadcd3ac466b929c9a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968369"
---
# <a name="eventtriggertype-complex-type"></a><span data-ttu-id="fc581-104">eventTriggerType 複雜類型</span><span class="sxs-lookup"><span data-stu-id="fc581-104">eventTriggerType Complex Type</span></span>

<span data-ttu-id="fc581-105">定義 [**EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md) 元素的子項目和排序資訊。</span><span class="sxs-lookup"><span data-stu-id="fc581-105">Defines the child elements and sequencing information for the [**EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md) element.</span></span>

``` syntax
<xs:complexType name="eventTriggerType">
    <xs:complexContent>
        <xs:extension
            base="triggerBaseType"
        >
            <xs:sequence>
                <xs:element name="Subscription"
                    type="nonEmptyString"
                 />
                <xs:element name="Delay"
                    type="duration"
                    default="PT0M"
                    minOccurs="0"
                 />
                <xs:element name="ValueQueries"
                    type="namedValues"
                    minOccurs="0"
                 />
            </xs:sequence>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="fc581-106">子元素</span><span class="sxs-lookup"><span data-stu-id="fc581-106">Child elements</span></span>



| <span data-ttu-id="fc581-107">元素</span><span class="sxs-lookup"><span data-stu-id="fc581-107">Element</span></span>                                                                           | <span data-ttu-id="fc581-108">類型</span><span class="sxs-lookup"><span data-stu-id="fc581-108">Type</span></span>                                                                    | <span data-ttu-id="fc581-109">Description</span><span class="sxs-lookup"><span data-stu-id="fc581-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fc581-110">**延遲**</span><span class="sxs-lookup"><span data-stu-id="fc581-110">**Delay**</span></span>](taskschedulerschema-delay-eventtriggertype-element.md)               | <span data-ttu-id="fc581-111">duration</span><span class="sxs-lookup"><span data-stu-id="fc581-111">duration</span></span>                                                                | <span data-ttu-id="fc581-112">指定事件發生時間和工作啟動時間之間的時間量。</span><span class="sxs-lookup"><span data-stu-id="fc581-112">Specifies the amount of time between when the event occurs and when the task is started.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="fc581-113">**訂用帳戶**</span><span class="sxs-lookup"><span data-stu-id="fc581-113">**Subscription**</span></span>](taskschedulerschema-subscription-eventtriggertype-element.md) | [<span data-ttu-id="fc581-114">**nonEmptyString**</span><span class="sxs-lookup"><span data-stu-id="fc581-114">**nonEmptyString**</span></span>](taskschedulerschema-nonemptystring-simpletype.md) | <span data-ttu-id="fc581-115">指定 XPath 查詢，以識別引發觸發程式的事件。</span><span class="sxs-lookup"><span data-stu-id="fc581-115">Specifies the XPath query that identifies the event that fires the trigger.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [<span data-ttu-id="fc581-116">**ValueQueries**</span><span class="sxs-lookup"><span data-stu-id="fc581-116">**ValueQueries**</span></span>](taskschedulerschema-valuequeries-eventtriggertype-element.md) | [<span data-ttu-id="fc581-117">**namedValues**</span><span class="sxs-lookup"><span data-stu-id="fc581-117">**namedValues**</span></span>](taskschedulerschema-namedvalues-complextype.md)      | <span data-ttu-id="fc581-118">指定每個專案的序列，其中每個元素都包含名稱和 XPath 查詢值。</span><span class="sxs-lookup"><span data-stu-id="fc581-118">Specifies a sequence of elements that each contain a name and an XPath query value.</span></span> <span data-ttu-id="fc581-119">查詢會套用至從 [**訂**](taskschedulerschema-subscription-eventtriggertype-element.md) 用帳戶元素中指定之事件訂閱傳回的事件。</span><span class="sxs-lookup"><span data-stu-id="fc581-119">The queries are applied to an event returned from the event subscription specified in the [**Subscription**](taskschedulerschema-subscription-eventtriggertype-element.md) element.</span></span> <span data-ttu-id="fc581-120">XPath 查詢值的名稱可做為工作的 [ [**ShowMessage**](taskschedulerschema-showmessage-actiongroup-element.md)動作] 區段中的 [ [**Body**](taskschedulerschema-body-showmessagetype-element.md) ] 元素中的變數。</span><span class="sxs-lookup"><span data-stu-id="fc581-120">The name for the XPath query value can be used as a variable in the [**Body**](taskschedulerschema-body-showmessagetype-element.md) element in the [**ShowMessage**](taskschedulerschema-showmessage-actiongroup-element.md) action section of a task.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="fc581-121">備註</span><span class="sxs-lookup"><span data-stu-id="fc581-121">Remarks</span></span>

<span data-ttu-id="fc581-122">除了這裡定義的子項目之外， [**EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md) 元素也會使用 [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) 複雜類型所定義的子專案。</span><span class="sxs-lookup"><span data-stu-id="fc581-122">In addition to the child element defined here, the [**EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md) element also uses child elements defined by the [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc581-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="fc581-123">Requirements</span></span>



| <span data-ttu-id="fc581-124">需求</span><span class="sxs-lookup"><span data-stu-id="fc581-124">Requirement</span></span> | <span data-ttu-id="fc581-125">值</span><span class="sxs-lookup"><span data-stu-id="fc581-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="fc581-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fc581-126">Minimum supported client</span></span><br/> | <span data-ttu-id="fc581-127">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fc581-127">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="fc581-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fc581-128">Minimum supported server</span></span><br/> | <span data-ttu-id="fc581-129">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fc581-129">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fc581-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fc581-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc581-131">工作排程器架構複雜類型</span><span class="sxs-lookup"><span data-stu-id="fc581-131">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="fc581-132">工作排程器</span><span class="sxs-lookup"><span data-stu-id="fc581-132">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





