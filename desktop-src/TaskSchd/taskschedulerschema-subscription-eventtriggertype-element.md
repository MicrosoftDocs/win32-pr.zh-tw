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
# <a name="subscription-eventtriggertype-element"></a><span data-ttu-id="8bf52-104">訂用帳戶 (eventTriggerType) 元素</span><span class="sxs-lookup"><span data-stu-id="8bf52-104">Subscription (eventTriggerType) Element</span></span>

<span data-ttu-id="8bf52-105">指定 XPath 查詢，以識別引發觸發程式的事件。</span><span class="sxs-lookup"><span data-stu-id="8bf52-105">Specifies the XPath query that identifies the event that fires the trigger.</span></span>

``` syntax
<xs:element name="Subscription"
    type="nonEmptyString"
 />
```

<span data-ttu-id="8bf52-106">**訂** 用帳戶元素是由 [**eventTriggerType**](taskschedulerschema-eventtriggertype-complextype.md)複雜型別所定義。</span><span class="sxs-lookup"><span data-stu-id="8bf52-106">The **Subscription** element is defined by the [**eventTriggerType**](taskschedulerschema-eventtriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="8bf52-107">父元素</span><span class="sxs-lookup"><span data-stu-id="8bf52-107">Parent element</span></span>



| <span data-ttu-id="8bf52-108">元素</span><span class="sxs-lookup"><span data-stu-id="8bf52-108">Element</span></span>                                                                       | <span data-ttu-id="8bf52-109">衍生自</span><span class="sxs-lookup"><span data-stu-id="8bf52-109">Derived from</span></span>                                                                 | <span data-ttu-id="8bf52-110">Description</span><span class="sxs-lookup"><span data-stu-id="8bf52-110">Description</span></span>                                                                   |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [<span data-ttu-id="8bf52-111">**EventTrigger**</span><span class="sxs-lookup"><span data-stu-id="8bf52-111">**EventTrigger**</span></span>](taskschedulerschema-eventtrigger-triggergroup-element.md) | [<span data-ttu-id="8bf52-112">**eventTriggerType**</span><span class="sxs-lookup"><span data-stu-id="8bf52-112">**eventTriggerType**</span></span>](taskschedulerschema-eventtriggertype-complextype.md) | <span data-ttu-id="8bf52-113">指定在發生系統事件時啟動工作的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="8bf52-113">Specifies a trigger that starts a task when a system event occurs.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="8bf52-114">備註</span><span class="sxs-lookup"><span data-stu-id="8bf52-114">Remarks</span></span>

<span data-ttu-id="8bf52-115">針對腳本開發，事件訂閱是由 [ [**EventTrigger**](eventtrigger-subscription.md) ] 屬性所指定。</span><span class="sxs-lookup"><span data-stu-id="8bf52-115">For script development, the event subscription is specified by the [**EventTrigger.Subscription**](eventtrigger-subscription.md) property.</span></span>

<span data-ttu-id="8bf52-116">針對 c + + 開發，事件訂閱是由 [**IEventTrigger：：訂**](/windows/desktop/api/taskschd/nf-taskschd-ieventtrigger-get_subscription) 用帳戶屬性所指定。</span><span class="sxs-lookup"><span data-stu-id="8bf52-116">For C++ development, the event subscription is specified by the [**IEventTrigger::Subscription**](/windows/desktop/api/taskschd/nf-taskschd-ieventtrigger-get_subscription) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="8bf52-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="8bf52-117">Requirements</span></span>



| <span data-ttu-id="8bf52-118">需求</span><span class="sxs-lookup"><span data-stu-id="8bf52-118">Requirement</span></span> | <span data-ttu-id="8bf52-119">值</span><span class="sxs-lookup"><span data-stu-id="8bf52-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="8bf52-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8bf52-120">Minimum supported client</span></span><br/> | <span data-ttu-id="8bf52-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8bf52-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="8bf52-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8bf52-122">Minimum supported server</span></span><br/> | <span data-ttu-id="8bf52-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8bf52-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8bf52-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8bf52-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8bf52-125">工作排程器架構元素</span><span class="sxs-lookup"><span data-stu-id="8bf52-125">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="8bf52-126">工作排程器</span><span class="sxs-lookup"><span data-stu-id="8bf52-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





