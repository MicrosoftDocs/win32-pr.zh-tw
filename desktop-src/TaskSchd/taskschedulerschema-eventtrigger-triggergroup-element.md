---
title: EventTrigger (triggerGroup) 元素
description: 指定在發生系統事件時啟動工作的觸發程式。
ms.assetid: 8faffc04-1ad2-499d-bcdf-bc28f64b8aa8
keywords:
- 事件觸發程式工作排程器，元素
- EventTrigger 元素工作排程器
topic_type:
- apiref
api_name:
- EventTrigger
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3cecf46250fface0f716adbf287cda3269b86f04
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466284"
---
# <a name="eventtrigger-triggergroup-element"></a><span data-ttu-id="7f931-105">EventTrigger (triggerGroup) 元素</span><span class="sxs-lookup"><span data-stu-id="7f931-105">EventTrigger (triggerGroup) Element</span></span>

<span data-ttu-id="7f931-106">指定在發生系統事件時啟動工作的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="7f931-106">Specifies a trigger that starts a task when a system event occurs.</span></span>

``` syntax
<xs:element name="EventTrigger"
    type="eventTriggerType"
 />
```

<span data-ttu-id="7f931-107">**EventTrigger** 元素是由 [**triggerGroup**](taskschedulerschema-triggergroup-group.md)定義。</span><span class="sxs-lookup"><span data-stu-id="7f931-107">The **EventTrigger** element is defined by the [**triggerGroup**](taskschedulerschema-triggergroup-group.md) .</span></span>

## <a name="parent-element"></a><span data-ttu-id="7f931-108">父元素</span><span class="sxs-lookup"><span data-stu-id="7f931-108">Parent element</span></span>



| <span data-ttu-id="7f931-109">元素</span><span class="sxs-lookup"><span data-stu-id="7f931-109">Element</span></span>                                                           | <span data-ttu-id="7f931-110">衍生自</span><span class="sxs-lookup"><span data-stu-id="7f931-110">Derived from</span></span>                                                         | <span data-ttu-id="7f931-111">Description</span><span class="sxs-lookup"><span data-stu-id="7f931-111">Description</span></span>                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="7f931-112">**觸發程序**</span><span class="sxs-lookup"><span data-stu-id="7f931-112">**Triggers**</span></span>](taskschedulerschema-triggers-tasktype-element.md) | [<span data-ttu-id="7f931-113">**triggersType**</span><span class="sxs-lookup"><span data-stu-id="7f931-113">**triggersType**</span></span>](taskschedulerschema-triggerstype-complextype.md) | <span data-ttu-id="7f931-114">指定啟動工作的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="7f931-114">Specifies the triggers that start the task.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="7f931-115">子元素</span><span class="sxs-lookup"><span data-stu-id="7f931-115">Child elements</span></span>



| <span data-ttu-id="7f931-116">元素</span><span class="sxs-lookup"><span data-stu-id="7f931-116">Element</span></span>                                                                                              | <span data-ttu-id="7f931-117">類型</span><span class="sxs-lookup"><span data-stu-id="7f931-117">Type</span></span>                                                                     | <span data-ttu-id="7f931-118">Description</span><span class="sxs-lookup"><span data-stu-id="7f931-118">Description</span></span>                                                                                                                        |
|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7f931-119">**延遲 (eventTriggerType)**</span><span class="sxs-lookup"><span data-stu-id="7f931-119">**Delay (eventTriggerType)**</span></span>](taskschedulerschema-delay-eventtriggertype-element.md)               | <span data-ttu-id="7f931-120">duration</span><span class="sxs-lookup"><span data-stu-id="7f931-120">duration</span></span>                                                                 | <span data-ttu-id="7f931-121">指定事件發生時間和工作啟動時間之間的時間量。</span><span class="sxs-lookup"><span data-stu-id="7f931-121">Specifies the amount of time between when the event occurs and when the task is started.</span></span><br/>                                |
| [<span data-ttu-id="7f931-122">**已啟用 (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="7f931-122">**Enabled (triggerBaseType)**</span></span>](taskschedulerschema-enabled-triggerbasetype-element.md)             | <span data-ttu-id="7f931-123">boolean</span><span class="sxs-lookup"><span data-stu-id="7f931-123">boolean</span></span>                                                                  | <span data-ttu-id="7f931-124">指定啟用觸發程序。</span><span class="sxs-lookup"><span data-stu-id="7f931-124">Specifies that the trigger is enabled.</span></span><br/>                                                                                  |
| [<span data-ttu-id="7f931-125">**EndBoundary (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="7f931-125">**EndBoundary (triggerBaseType)**</span></span>](taskschedulerschema-endboundary-triggerbasetype-element.md)     | <span data-ttu-id="7f931-126">dateTime</span><span class="sxs-lookup"><span data-stu-id="7f931-126">dateTime</span></span>                                                                 | <span data-ttu-id="7f931-127">指定停用觸發程式的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="7f931-127">Specifies the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="7f931-128">觸發程式在停用之後無法啟動工作。</span><span class="sxs-lookup"><span data-stu-id="7f931-128">The trigger cannot start the task after it is deactivated.</span></span><br/> |
| [<span data-ttu-id="7f931-129">**重複 (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="7f931-129">**Repetition (triggerBaseType)**</span></span>](taskschedulerschema-repetition-triggerbasetype-element.md)       | [<span data-ttu-id="7f931-130">**repetitionType**</span><span class="sxs-lookup"><span data-stu-id="7f931-130">**repetitionType**</span></span>](taskschedulerschema-repetitiontype-complextype.md) | <span data-ttu-id="7f931-131">指定執行工作的頻率，以及啟動工作之後重複模式重複的時間長度。</span><span class="sxs-lookup"><span data-stu-id="7f931-131">Specifies how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/>          |
| [<span data-ttu-id="7f931-132">**StartBoundary (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="7f931-132">**StartBoundary (triggerBaseType)**</span></span>](taskschedulerschema-startboundary-triggerbasetype-element.md) | <span data-ttu-id="7f931-133">dateTime</span><span class="sxs-lookup"><span data-stu-id="7f931-133">dateTime</span></span>                                                                 | <span data-ttu-id="7f931-134">指定啟動觸發程式的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="7f931-134">Specifies the date and time when the trigger is activated.</span></span><br/>                                                              |
| [<span data-ttu-id="7f931-135">**訂用帳戶 (eventTriggerType)**</span><span class="sxs-lookup"><span data-stu-id="7f931-135">**Subscription (eventTriggerType)**</span></span>](taskschedulerschema-subscription-eventtriggertype-element.md) | <span data-ttu-id="7f931-136">字串</span><span class="sxs-lookup"><span data-stu-id="7f931-136">string</span></span>                                                                   | <span data-ttu-id="7f931-137">指定 XPath 查詢，以識別引發觸發程式的事件。</span><span class="sxs-lookup"><span data-stu-id="7f931-137">Specifies the XPath query that identifies the event that fires the trigger.</span></span><br/>                                             |



## <a name="attributes"></a><span data-ttu-id="7f931-138">屬性</span><span class="sxs-lookup"><span data-stu-id="7f931-138">Attributes</span></span>



| <span data-ttu-id="7f931-139">名稱</span><span class="sxs-lookup"><span data-stu-id="7f931-139">Name</span></span> | <span data-ttu-id="7f931-140">類型</span><span class="sxs-lookup"><span data-stu-id="7f931-140">Type</span></span> | <span data-ttu-id="7f931-141">Description</span><span class="sxs-lookup"><span data-stu-id="7f931-141">Description</span></span>                           |
|------|------|---------------------------------------|
| <span data-ttu-id="7f931-142">識別碼</span><span class="sxs-lookup"><span data-stu-id="7f931-142">Id</span></span>   | <span data-ttu-id="7f931-143">識別碼</span><span class="sxs-lookup"><span data-stu-id="7f931-143">ID</span></span>   | <span data-ttu-id="7f931-144">觸發程式的識別碼。</span><span class="sxs-lookup"><span data-stu-id="7f931-144">Identifier of the trigger.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="7f931-145">備註</span><span class="sxs-lookup"><span data-stu-id="7f931-145">Remarks</span></span>

<span data-ttu-id="7f931-146">您可以建立最多500個具有事件訂閱的工作。</span><span class="sxs-lookup"><span data-stu-id="7f931-146">A maximum of 500 tasks with event subscriptions can be created.</span></span> <span data-ttu-id="7f931-147">針對各種事件進行查詢的事件訂閱，可以用來觸發使用相同動作來回應所記錄事件的工作。</span><span class="sxs-lookup"><span data-stu-id="7f931-147">An event subscription that queries for a variety of events can be used to trigger a task that uses the same action in response to the events being logged.</span></span>

<span data-ttu-id="7f931-148">針對腳本開發，事件觸發程式是由 [**EventTrigger**](eventtrigger.md) 物件所定義。</span><span class="sxs-lookup"><span data-stu-id="7f931-148">For script development, an event trigger is defined by the [**EventTrigger**](eventtrigger.md) object.</span></span>

<span data-ttu-id="7f931-149">針對 c + + 開發，事件觸發程式是由 [**IEventTrigger**](/windows/desktop/api/taskschd/nn-taskschd-ieventtrigger) 介面所定義。</span><span class="sxs-lookup"><span data-stu-id="7f931-149">For C++ development, an event trigger is defined by the [**IEventTrigger**](/windows/desktop/api/taskschd/nn-taskschd-ieventtrigger) interface.</span></span>

## <a name="examples"></a><span data-ttu-id="7f931-150">範例</span><span class="sxs-lookup"><span data-stu-id="7f931-150">Examples</span></span>

<span data-ttu-id="7f931-151">如需使用事件觸發程式之 XML 的完整範例，請參閱 [事件觸發程式範例 (xml) ](/previous-versions//aa446889(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="7f931-151">For a complete example of the XML for a task that uses an event trigger, see [Event Trigger Example (XML)](/previous-versions//aa446889(v=vs.85)).</span></span>

## <a name="requirements"></a><span data-ttu-id="7f931-152">規格需求</span><span class="sxs-lookup"><span data-stu-id="7f931-152">Requirements</span></span>



| <span data-ttu-id="7f931-153">需求</span><span class="sxs-lookup"><span data-stu-id="7f931-153">Requirement</span></span> | <span data-ttu-id="7f931-154">值</span><span class="sxs-lookup"><span data-stu-id="7f931-154">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7f931-155">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7f931-155">Minimum supported client</span></span><br/> | <span data-ttu-id="7f931-156">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7f931-156">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="7f931-157">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7f931-157">Minimum supported server</span></span><br/> | <span data-ttu-id="7f931-158">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7f931-158">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7f931-159">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7f931-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f931-160">工作排程器</span><span class="sxs-lookup"><span data-stu-id="7f931-160">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

