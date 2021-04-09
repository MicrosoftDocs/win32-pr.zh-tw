---
title: 訂用帳戶 (eventTriggerType) 元素
description: 指定 XPath 查詢，以識別引發觸發程式的事件。
ms.assetid: ea351a55-c6f9-4e39-b15e-c2a1027a1360
keywords:
- 訂用帳戶元素工作排程器
topic_type:
- apiref
api_name:
- Subscription
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: efe38f2e825e2de566391a7b1707ce1f8cfbbc68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686560"
---
# <a name="subscription-eventtriggertype-element"></a><span data-ttu-id="53df2-104">訂用帳戶 (eventTriggerType) 元素</span><span class="sxs-lookup"><span data-stu-id="53df2-104">Subscription (eventTriggerType) Element</span></span>

<span data-ttu-id="53df2-105">指定 XPath 查詢，以識別引發觸發程式的事件。</span><span class="sxs-lookup"><span data-stu-id="53df2-105">Specifies the XPath query that identifies the event that fires the trigger.</span></span>

``` syntax
<xs:element name="Subscription"
    type="nonEmptyString"
 />
```

<span data-ttu-id="53df2-106">**訂** 用帳戶元素是由 [**eventTriggerType**](taskschedulerschema-eventtriggertype-complextype.md)複雜型別所定義。</span><span class="sxs-lookup"><span data-stu-id="53df2-106">The **Subscription** element is defined by the [**eventTriggerType**](taskschedulerschema-eventtriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="53df2-107">父元素</span><span class="sxs-lookup"><span data-stu-id="53df2-107">Parent element</span></span>



| <span data-ttu-id="53df2-108">元素</span><span class="sxs-lookup"><span data-stu-id="53df2-108">Element</span></span>                                                                       | <span data-ttu-id="53df2-109">衍生自</span><span class="sxs-lookup"><span data-stu-id="53df2-109">Derived from</span></span>                                                                 | <span data-ttu-id="53df2-110">Description</span><span class="sxs-lookup"><span data-stu-id="53df2-110">Description</span></span>                                                                   |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [<span data-ttu-id="53df2-111">**EventTrigger**</span><span class="sxs-lookup"><span data-stu-id="53df2-111">**EventTrigger**</span></span>](taskschedulerschema-eventtrigger-triggergroup-element.md) | [<span data-ttu-id="53df2-112">**eventTriggerType**</span><span class="sxs-lookup"><span data-stu-id="53df2-112">**eventTriggerType**</span></span>](taskschedulerschema-eventtriggertype-complextype.md) | <span data-ttu-id="53df2-113">指定在發生系統事件時啟動工作的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="53df2-113">Specifies a trigger that starts a task when a system event occurs.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="53df2-114">備註</span><span class="sxs-lookup"><span data-stu-id="53df2-114">Remarks</span></span>

<span data-ttu-id="53df2-115">針對腳本開發，事件訂閱是由 [ [**EventTrigger**](eventtrigger-subscription.md) ] 屬性所指定。</span><span class="sxs-lookup"><span data-stu-id="53df2-115">For script development, the event subscription is specified by the [**EventTrigger.Subscription**](eventtrigger-subscription.md) property.</span></span>

<span data-ttu-id="53df2-116">針對 c + + 開發，事件訂閱是由 [**IEventTrigger：：訂**](/windows/desktop/api/taskschd/nf-taskschd-ieventtrigger-get_subscription) 用帳戶屬性所指定。</span><span class="sxs-lookup"><span data-stu-id="53df2-116">For C++ development, the event subscription is specified by the [**IEventTrigger::Subscription**](/windows/desktop/api/taskschd/nf-taskschd-ieventtrigger-get_subscription) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="53df2-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="53df2-117">Requirements</span></span>



| <span data-ttu-id="53df2-118">需求</span><span class="sxs-lookup"><span data-stu-id="53df2-118">Requirement</span></span> | <span data-ttu-id="53df2-119">值</span><span class="sxs-lookup"><span data-stu-id="53df2-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="53df2-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="53df2-120">Minimum supported client</span></span><br/> | <span data-ttu-id="53df2-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="53df2-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="53df2-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="53df2-122">Minimum supported server</span></span><br/> | <span data-ttu-id="53df2-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="53df2-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="53df2-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="53df2-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53df2-125">工作排程器架構元素</span><span class="sxs-lookup"><span data-stu-id="53df2-125">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="53df2-126">工作排程器</span><span class="sxs-lookup"><span data-stu-id="53df2-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





