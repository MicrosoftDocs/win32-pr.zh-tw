---
title: 觸發程式 (taskType) 元素
description: 指定啟動工作的觸發程式。
ms.assetid: 4bf8e85e-3742-433d-821f-736fb2ff7139
keywords:
- 觸發程式元素工作排程器
topic_type:
- apiref
api_name:
- Triggers
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 06994c395fbfbc5b0c6244c9d17930bc4afac885
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686555"
---
# <a name="triggers-tasktype-element"></a><span data-ttu-id="e84a5-104">觸發程式 (taskType) 元素</span><span class="sxs-lookup"><span data-stu-id="e84a5-104">Triggers (taskType) Element</span></span>

<span data-ttu-id="e84a5-105">指定啟動工作的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="e84a5-105">Specifies the triggers that start the task.</span></span>

``` syntax
<xs:element name="Triggers"
    type="triggersType"
 />
```

<span data-ttu-id="e84a5-106">**觸發** 程式元素是由 [**triggersType**](taskschedulerschema-triggerstype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="e84a5-106">The **Triggers** element is defined by the [**triggersType**](taskschedulerschema-triggerstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="e84a5-107">父元素</span><span class="sxs-lookup"><span data-stu-id="e84a5-107">Parent element</span></span>



| <span data-ttu-id="e84a5-108">元素</span><span class="sxs-lookup"><span data-stu-id="e84a5-108">Element</span></span>                                          | <span data-ttu-id="e84a5-109">衍生自</span><span class="sxs-lookup"><span data-stu-id="e84a5-109">Derived from</span></span>                                                 | <span data-ttu-id="e84a5-110">Description</span><span class="sxs-lookup"><span data-stu-id="e84a5-110">Description</span></span>                                                                  |
|--------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------------|
| [<span data-ttu-id="e84a5-111">**Task**</span><span class="sxs-lookup"><span data-stu-id="e84a5-111">**Task**</span></span>](taskschedulerschema-task-element.md) | [<span data-ttu-id="e84a5-112">**taskType**</span><span class="sxs-lookup"><span data-stu-id="e84a5-112">**taskType**</span></span>](taskschedulerschema-tasktype-complextype.md) | <span data-ttu-id="e84a5-113">定義工作排程器服務所執行的工作。</span><span class="sxs-lookup"><span data-stu-id="e84a5-113">Defines the task that is performed by the Task Scheduler service.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="e84a5-114">子元素</span><span class="sxs-lookup"><span data-stu-id="e84a5-114">Child elements</span></span>



| <span data-ttu-id="e84a5-115">元素</span><span class="sxs-lookup"><span data-stu-id="e84a5-115">Element</span></span>                                                                                     | <span data-ttu-id="e84a5-116">類型</span><span class="sxs-lookup"><span data-stu-id="e84a5-116">Type</span></span>                                                                                       | <span data-ttu-id="e84a5-117">Description</span><span class="sxs-lookup"><span data-stu-id="e84a5-117">Description</span></span>                                                                                  |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e84a5-118">**BootTrigger**</span><span class="sxs-lookup"><span data-stu-id="e84a5-118">**BootTrigger**</span></span>](taskschedulerschema-boottrigger-triggergroup-element.md)                 | [<span data-ttu-id="e84a5-119">**bootTriggerType**</span><span class="sxs-lookup"><span data-stu-id="e84a5-119">**bootTriggerType**</span></span>](taskschedulerschema-boottriggertype-complextype.md)                 | <span data-ttu-id="e84a5-120">指定啟動系統時啟動工作的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="e84a5-120">Specifies a trigger that starts a task when the system is booted.</span></span><br/>                 |
| [<span data-ttu-id="e84a5-121">**CalendarTrigger**</span><span class="sxs-lookup"><span data-stu-id="e84a5-121">**CalendarTrigger**</span></span>](taskschedulerschema-calendartrigger-triggergroup-element.md)         | [<span data-ttu-id="e84a5-122">**calendarTriggerType**</span><span class="sxs-lookup"><span data-stu-id="e84a5-122">**calendarTriggerType**</span></span>](taskschedulerschema-calendartriggertype-complextype.md)         | <span data-ttu-id="e84a5-123">指定每日、每週、每月或每週 (DOW) 觸發程式。</span><span class="sxs-lookup"><span data-stu-id="e84a5-123">Specifies a daily, weekly, monthly, or a monthly day-of-the-week (DOW) trigger.</span></span><br/>   |
| [<span data-ttu-id="e84a5-124">**EventTrigger**</span><span class="sxs-lookup"><span data-stu-id="e84a5-124">**EventTrigger**</span></span>](taskschedulerschema-eventtrigger-triggergroup-element.md)               | [<span data-ttu-id="e84a5-125">**eventTriggerType**</span><span class="sxs-lookup"><span data-stu-id="e84a5-125">**eventTriggerType**</span></span>](taskschedulerschema-eventtriggertype-complextype.md)               | <span data-ttu-id="e84a5-126">指定在發生系統事件時啟動工作的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="e84a5-126">Specifies a trigger that starts a task when a system event occurs.</span></span><br/>                |
| [<span data-ttu-id="e84a5-127">**IdleTrigger**</span><span class="sxs-lookup"><span data-stu-id="e84a5-127">**IdleTrigger**</span></span>](taskschedulerschema-idletrigger-triggergroup-element.md)                 | [<span data-ttu-id="e84a5-128">**idleTriggerType**</span><span class="sxs-lookup"><span data-stu-id="e84a5-128">**idleTriggerType**</span></span>](taskschedulerschema-idletriggertype-complextype.md)                 | <span data-ttu-id="e84a5-129">指定當電腦進入閒置狀態時啟動工作的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="e84a5-129">Specifies a trigger that starts a task when the computer goes into an idle state.</span></span><br/> |
| [<span data-ttu-id="e84a5-130">**LogonTrigger**</span><span class="sxs-lookup"><span data-stu-id="e84a5-130">**LogonTrigger**</span></span>](taskschedulerschema-logontrigger-triggergroup-element.md)               | [<span data-ttu-id="e84a5-131">**logonTriggerType**</span><span class="sxs-lookup"><span data-stu-id="e84a5-131">**logonTriggerType**</span></span>](taskschedulerschema-logontriggertype-complextype.md)               | <span data-ttu-id="e84a5-132">指定當使用者登入時啟動工作的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="e84a5-132">Specifies a trigger that starts a task when a user logs on.</span></span><br/>                       |
| [<span data-ttu-id="e84a5-133">**RegistrationTrigger**</span><span class="sxs-lookup"><span data-stu-id="e84a5-133">**RegistrationTrigger**</span></span>](taskschedulerschema-registrationtrigger-triggergroup-element.md) | [<span data-ttu-id="e84a5-134">**registrationTriggerType**</span><span class="sxs-lookup"><span data-stu-id="e84a5-134">**registrationTriggerType**</span></span>](taskschedulerschema-registrationtriggertype-complextype.md) | <span data-ttu-id="e84a5-135">指定在註冊工作時啟動工作的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="e84a5-135">Specifies a trigger that starts a task when the task is registered.</span></span><br/>               |
| [<span data-ttu-id="e84a5-136">**TimeTrigger**</span><span class="sxs-lookup"><span data-stu-id="e84a5-136">**TimeTrigger**</span></span>](taskschedulerschema-timetrigger-triggergroup-element.md)                 | [<span data-ttu-id="e84a5-137">**timeTriggerType**</span><span class="sxs-lookup"><span data-stu-id="e84a5-137">**timeTriggerType**</span></span>](taskschedulerschema-timetriggertype-complextype.md)                 | <span data-ttu-id="e84a5-138">指定啟動觸發程式時啟動工作的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="e84a5-138">Specifies a trigger that starts a task when the trigger is activated.</span></span><br/>             |



## <a name="remarks"></a><span data-ttu-id="e84a5-139">備註</span><span class="sxs-lookup"><span data-stu-id="e84a5-139">Remarks</span></span>

<span data-ttu-id="e84a5-140">您可以依任何順序加入上列的子項目。</span><span class="sxs-lookup"><span data-stu-id="e84a5-140">The child elements listed above can be added in any order.</span></span>

<span data-ttu-id="e84a5-141">針對 c + + 開發，會使用 [**ITaskDefinition 的 trigger 屬性**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_triggers)來指定工作的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="e84a5-141">For C++ development, the triggers of a task are specified using the [**Triggers property of ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_triggers).</span></span>

<span data-ttu-id="e84a5-142">針對開發腳本，會使用 [**TaskDefinition**](taskdefinition-triggers.md) 屬性來指定工作的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="e84a5-142">For scripting development, the triggers of a task are specified using the [**TaskDefinition.Triggers**](taskdefinition-triggers.md) property.</span></span>

## <a name="examples"></a><span data-ttu-id="e84a5-143">範例</span><span class="sxs-lookup"><span data-stu-id="e84a5-143">Examples</span></span>

<span data-ttu-id="e84a5-144">如需指定觸發程式之工作的完整 XML 範例，請參閱 [時間觸發程式範例 (xml) ](time-trigger-example--xml-.md)。</span><span class="sxs-lookup"><span data-stu-id="e84a5-144">For a complete example of the XML for a task that specifies a trigger, see [Time Trigger Example (XML)](time-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e84a5-145">規格需求</span><span class="sxs-lookup"><span data-stu-id="e84a5-145">Requirements</span></span>



| <span data-ttu-id="e84a5-146">需求</span><span class="sxs-lookup"><span data-stu-id="e84a5-146">Requirement</span></span> | <span data-ttu-id="e84a5-147">值</span><span class="sxs-lookup"><span data-stu-id="e84a5-147">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e84a5-148">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e84a5-148">Minimum supported client</span></span><br/> | <span data-ttu-id="e84a5-149">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e84a5-149">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e84a5-150">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e84a5-150">Minimum supported server</span></span><br/> | <span data-ttu-id="e84a5-151">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e84a5-151">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e84a5-152">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e84a5-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e84a5-153">工作排程器架構元素</span><span class="sxs-lookup"><span data-stu-id="e84a5-153">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="e84a5-154">工作排程器</span><span class="sxs-lookup"><span data-stu-id="e84a5-154">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





