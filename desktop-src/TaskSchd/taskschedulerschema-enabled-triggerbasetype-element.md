---
title: 已啟用 (triggerBaseType) 元素
description: 指定啟用觸發程序。
ms.assetid: 14c98f40-0ec5-4dc1-978e-b02c08ee2384
keywords:
- Enabled 元素工作排程器
topic_type:
- apiref
api_name:
- Enabled
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 42b495ba1af5f3b9b99034b0d6ca9d02040460c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025489"
---
# <a name="enabled-triggerbasetype-element"></a><span data-ttu-id="c0d9f-104">已啟用 (triggerBaseType) 元素</span><span class="sxs-lookup"><span data-stu-id="c0d9f-104">Enabled (triggerBaseType) Element</span></span>

<span data-ttu-id="c0d9f-105">指定啟用觸發程序。</span><span class="sxs-lookup"><span data-stu-id="c0d9f-105">Specifies that the trigger is enabled.</span></span>

``` syntax
<xs:element name="Enabled"
    type="boolean"
 />
```

<span data-ttu-id="c0d9f-106">**Enabled** 元素是由 [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="c0d9f-106">The **Enabled** element is defined by the [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="c0d9f-107">父元素</span><span class="sxs-lookup"><span data-stu-id="c0d9f-107">Parent element</span></span>



| <span data-ttu-id="c0d9f-108">元素</span><span class="sxs-lookup"><span data-stu-id="c0d9f-108">Element</span></span>                                                                                     | <span data-ttu-id="c0d9f-109">衍生自</span><span class="sxs-lookup"><span data-stu-id="c0d9f-109">Derived from</span></span>                                                                               | <span data-ttu-id="c0d9f-110">Description</span><span class="sxs-lookup"><span data-stu-id="c0d9f-110">Description</span></span>                                                                                  |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c0d9f-111">**BootTrigger**</span><span class="sxs-lookup"><span data-stu-id="c0d9f-111">**BootTrigger**</span></span>](taskschedulerschema-boottrigger-triggergroup-element.md)                 | [<span data-ttu-id="c0d9f-112">**bootTriggerType**</span><span class="sxs-lookup"><span data-stu-id="c0d9f-112">**bootTriggerType**</span></span>](taskschedulerschema-boottriggertype-complextype.md)                 | <span data-ttu-id="c0d9f-113">指定啟動系統時啟動工作的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="c0d9f-113">Specifies a trigger that starts a task when the system is booted.</span></span><br/>                 |
| [<span data-ttu-id="c0d9f-114">**CalendarTrigger**</span><span class="sxs-lookup"><span data-stu-id="c0d9f-114">**CalendarTrigger**</span></span>](taskschedulerschema-calendartrigger-triggergroup-element.md)         | [<span data-ttu-id="c0d9f-115">**calendarTriggerType**</span><span class="sxs-lookup"><span data-stu-id="c0d9f-115">**calendarTriggerType**</span></span>](taskschedulerschema-calendartriggertype-complextype.md)         | <span data-ttu-id="c0d9f-116">指定每日、每週、每月或每週 (DOW) 觸發程式。</span><span class="sxs-lookup"><span data-stu-id="c0d9f-116">Specifies a daily, weekly, monthly, or a monthly day-of-the-week (DOW) trigger.</span></span><br/>   |
| [<span data-ttu-id="c0d9f-117">**EventTrigger**</span><span class="sxs-lookup"><span data-stu-id="c0d9f-117">**EventTrigger**</span></span>](taskschedulerschema-eventtrigger-triggergroup-element.md)               | [<span data-ttu-id="c0d9f-118">**eventTriggerType**</span><span class="sxs-lookup"><span data-stu-id="c0d9f-118">**eventTriggerType**</span></span>](taskschedulerschema-eventtriggertype-complextype.md)               | <span data-ttu-id="c0d9f-119">指定在發生系統事件時啟動工作的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="c0d9f-119">Specifies a trigger that starts a task when a system event occurs.</span></span><br/>                |
| [<span data-ttu-id="c0d9f-120">**IdleTrigger**</span><span class="sxs-lookup"><span data-stu-id="c0d9f-120">**IdleTrigger**</span></span>](taskschedulerschema-idletrigger-triggergroup-element.md)                 | [<span data-ttu-id="c0d9f-121">**idleTriggerType**</span><span class="sxs-lookup"><span data-stu-id="c0d9f-121">**idleTriggerType**</span></span>](taskschedulerschema-idletriggertype-complextype.md)                 | <span data-ttu-id="c0d9f-122">指定當電腦進入閒置狀態時啟動工作的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="c0d9f-122">Specifies a trigger that starts a task when the computer goes into an idle state.</span></span><br/> |
| [<span data-ttu-id="c0d9f-123">**LogonTrigger**</span><span class="sxs-lookup"><span data-stu-id="c0d9f-123">**LogonTrigger**</span></span>](taskschedulerschema-logontrigger-triggergroup-element.md)               | [<span data-ttu-id="c0d9f-124">**logonTriggerType**</span><span class="sxs-lookup"><span data-stu-id="c0d9f-124">**logonTriggerType**</span></span>](taskschedulerschema-logontriggertype-complextype.md)               | <span data-ttu-id="c0d9f-125">指定當使用者登入時啟動工作的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="c0d9f-125">Specifies a trigger that starts a task when a user logs on.</span></span><br/>                       |
| [<span data-ttu-id="c0d9f-126">**RegistrationTrigger**</span><span class="sxs-lookup"><span data-stu-id="c0d9f-126">**RegistrationTrigger**</span></span>](taskschedulerschema-registrationtrigger-triggergroup-element.md) | [<span data-ttu-id="c0d9f-127">**registrationTriggerType**</span><span class="sxs-lookup"><span data-stu-id="c0d9f-127">**registrationTriggerType**</span></span>](taskschedulerschema-registrationtriggertype-complextype.md) | <span data-ttu-id="c0d9f-128">指定在註冊工作時啟動工作的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="c0d9f-128">Specifies a trigger that starts a task when the task is registered.</span></span><br/>               |
| [<span data-ttu-id="c0d9f-129">**TimeTrigger**</span><span class="sxs-lookup"><span data-stu-id="c0d9f-129">**TimeTrigger**</span></span>](taskschedulerschema-timetrigger-triggergroup-element.md)                 | [<span data-ttu-id="c0d9f-130">**timeTriggerType**</span><span class="sxs-lookup"><span data-stu-id="c0d9f-130">**timeTriggerType**</span></span>](taskschedulerschema-timetriggertype-complextype.md)                 | <span data-ttu-id="c0d9f-131">指定啟動觸發程式時啟動工作的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="c0d9f-131">Specifies a trigger that starts a task when the trigger is activated.</span></span><br/>             |



## <a name="remarks"></a><span data-ttu-id="c0d9f-132">備註</span><span class="sxs-lookup"><span data-stu-id="c0d9f-132">Remarks</span></span>

<span data-ttu-id="c0d9f-133">針對腳本開發，這項資訊是透過觸發程式來存取，所有觸發程式物件都會繼承 [**已啟用**](trigger-enabled.md) 的屬性。</span><span class="sxs-lookup"><span data-stu-id="c0d9f-133">For scripting development, this information is accessed through the [**Trigger.Enabled**](trigger-enabled.md) property that is inherited by the all trigger objects.</span></span>

<span data-ttu-id="c0d9f-134">針對 c + + 開發，這項資訊是透過所有觸發程式介面所繼承的 [**ITrigger：： Enabled**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_enabled) 屬性來存取。</span><span class="sxs-lookup"><span data-stu-id="c0d9f-134">For C++ development, this information is accessed through the [**ITrigger::Enabled**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_enabled) property that is inherited by the all trigger interfaces.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0d9f-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="c0d9f-135">Requirements</span></span>



| <span data-ttu-id="c0d9f-136">需求</span><span class="sxs-lookup"><span data-stu-id="c0d9f-136">Requirement</span></span> | <span data-ttu-id="c0d9f-137">值</span><span class="sxs-lookup"><span data-stu-id="c0d9f-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c0d9f-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c0d9f-138">Minimum supported client</span></span><br/> | <span data-ttu-id="c0d9f-139">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c0d9f-139">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c0d9f-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c0d9f-140">Minimum supported server</span></span><br/> | <span data-ttu-id="c0d9f-141">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c0d9f-141">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c0d9f-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c0d9f-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0d9f-143">工作排程器架構元素</span><span class="sxs-lookup"><span data-stu-id="c0d9f-143">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="c0d9f-144">工作排程器</span><span class="sxs-lookup"><span data-stu-id="c0d9f-144">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





