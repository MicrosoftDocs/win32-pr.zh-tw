---
title: triggerGroup 群組
description: 定義觸發程式群組。
ms.assetid: e07e6999-d982-405b-adfd-2976707b999f
keywords:
- triggerGroup 工作排程器
topic_type:
- apiref
api_name:
- triggerGroup
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ce0203cd9515808891f93223dd7b3ebaf2642103
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106343"
---
# <a name="triggergroup-group"></a><span data-ttu-id="3f918-104">triggerGroup 群組</span><span class="sxs-lookup"><span data-stu-id="3f918-104">triggerGroup Group</span></span>

<span data-ttu-id="3f918-105">定義觸發程式群組。</span><span class="sxs-lookup"><span data-stu-id="3f918-105">Defines the trigger group.</span></span>

``` syntax
<xs:group name="triggerGroup">
    <xs:choice>
        <xs:element name="BootTrigger"
            type="bootTriggerType"
            minOccurs="0"
         />
        <xs:element name="RegistrationTrigger"
            type="registrationTriggerType"
            minOccurs="0"
         />
        <xs:element name="IdleTrigger"
            type="idleTriggerType"
            minOccurs="0"
         />
        <xs:element name="TimeTrigger"
            type="timeTriggerType"
            minOccurs="0"
         />
        <xs:element name="EventTrigger"
            type="eventTriggerType"
            minOccurs="0"
         />
        <xs:element name="LogonTrigger"
            type="logonTriggerType"
            minOccurs="0"
         />
        <xs:element name="SessionStateChangeTrigger"
            type="sessionStateChangeTriggerType"
            minOccurs="0"
         />
        <xs:element name="CalendarTrigger"
            type="calendarTriggerType"
            minOccurs="0"
         />
    </xs:choice>
</xs:group>
```

## <a name="child-elements"></a><span data-ttu-id="3f918-106">子元素</span><span class="sxs-lookup"><span data-stu-id="3f918-106">Child elements</span></span>



| <span data-ttu-id="3f918-107">元素</span><span class="sxs-lookup"><span data-stu-id="3f918-107">Element</span></span>                                                                                                 | <span data-ttu-id="3f918-108">類型</span><span class="sxs-lookup"><span data-stu-id="3f918-108">Type</span></span>                                                                                                   | <span data-ttu-id="3f918-109">Description</span><span class="sxs-lookup"><span data-stu-id="3f918-109">Description</span></span>                                                                                                       |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3f918-110">**BootTrigger**</span><span class="sxs-lookup"><span data-stu-id="3f918-110">**BootTrigger**</span></span>](taskschedulerschema-boottrigger-triggergroup-element.md)                             | [<span data-ttu-id="3f918-111">**bootTriggerType**</span><span class="sxs-lookup"><span data-stu-id="3f918-111">**bootTriggerType**</span></span>](taskschedulerschema-boottriggertype-complextype.md)                             | <span data-ttu-id="3f918-112">啟動系統時啟動工作的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="3f918-112">A trigger that starts a task when the system is booted.</span></span><br/>                                                |
| [<span data-ttu-id="3f918-113">**CalendarTrigger**</span><span class="sxs-lookup"><span data-stu-id="3f918-113">**CalendarTrigger**</span></span>](taskschedulerschema-calendartrigger-triggergroup-element.md)                     | [<span data-ttu-id="3f918-114">**calendarTriggerType**</span><span class="sxs-lookup"><span data-stu-id="3f918-114">**calendarTriggerType**</span></span>](taskschedulerschema-calendartriggertype-complextype.md)                     | <span data-ttu-id="3f918-115">根據每日、每週、每月或每月星期幾啟動工作的觸發程式 (DOW) 排程。</span><span class="sxs-lookup"><span data-stu-id="3f918-115">A trigger that starts a task based on a daily, weekly, monthly, or monthly day-of-week (DOW) schedule.</span></span><br/> |
| [<span data-ttu-id="3f918-116">**EventTrigger**</span><span class="sxs-lookup"><span data-stu-id="3f918-116">**EventTrigger**</span></span>](taskschedulerschema-eventtrigger-triggergroup-element.md)                           | [<span data-ttu-id="3f918-117">**eventTriggerType**</span><span class="sxs-lookup"><span data-stu-id="3f918-117">**eventTriggerType**</span></span>](taskschedulerschema-eventtriggertype-complextype.md)                           | <span data-ttu-id="3f918-118">當系統事件發生時啟動工作的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="3f918-118">A trigger that starts a task when a system event occurs.</span></span><br/>                                               |
| [<span data-ttu-id="3f918-119">**IdleTrigger**</span><span class="sxs-lookup"><span data-stu-id="3f918-119">**IdleTrigger**</span></span>](taskschedulerschema-idletrigger-triggergroup-element.md)                             | [<span data-ttu-id="3f918-120">**idleTriggerType**</span><span class="sxs-lookup"><span data-stu-id="3f918-120">**idleTriggerType**</span></span>](taskschedulerschema-idletriggertype-complextype.md)                             | <span data-ttu-id="3f918-121">當電腦進入閒置狀態時啟動工作的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="3f918-121">A trigger that starts a task when the computer goes into an idle state.</span></span><br/>                                |
| [<span data-ttu-id="3f918-122">**LogonTrigger**</span><span class="sxs-lookup"><span data-stu-id="3f918-122">**LogonTrigger**</span></span>](taskschedulerschema-logontrigger-triggergroup-element.md)                           | [<span data-ttu-id="3f918-123">**logonTriggerType**</span><span class="sxs-lookup"><span data-stu-id="3f918-123">**logonTriggerType**</span></span>](taskschedulerschema-logontriggertype-complextype.md)                           | <span data-ttu-id="3f918-124">當使用者登入時啟動工作的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="3f918-124">A trigger that starts a task when a user logs on.</span></span><br/>                                                      |
| [<span data-ttu-id="3f918-125">**RegistrationTrigger**</span><span class="sxs-lookup"><span data-stu-id="3f918-125">**RegistrationTrigger**</span></span>](taskschedulerschema-registrationtrigger-triggergroup-element.md)             | [<span data-ttu-id="3f918-126">**registrationTriggerType**</span><span class="sxs-lookup"><span data-stu-id="3f918-126">**registrationTriggerType**</span></span>](taskschedulerschema-registrationtriggertype-complextype.md)             | <span data-ttu-id="3f918-127">在註冊工作時啟動工作的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="3f918-127">A trigger that starts a task when the task is registered.</span></span><br/>                                              |
| [<span data-ttu-id="3f918-128">**SessionStateChangeTrigger**</span><span class="sxs-lookup"><span data-stu-id="3f918-128">**SessionStateChangeTrigger**</span></span>](taskschedulerschema-sessionstatechangetrigger-triggergroup-element.md) | [<span data-ttu-id="3f918-129">**sessionStateChangeTriggerType**</span><span class="sxs-lookup"><span data-stu-id="3f918-129">**sessionStateChangeTriggerType**</span></span>](taskschedulerschema-sessionstatechangetriggertype-complextype.md) | <span data-ttu-id="3f918-130">當終端機伺服器會話變更狀態時，啟動工作的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="3f918-130">A trigger that starts a task when a Terminal Server session changes state.</span></span><br/>                             |
| [<span data-ttu-id="3f918-131">**TimeTrigger**</span><span class="sxs-lookup"><span data-stu-id="3f918-131">**TimeTrigger**</span></span>](taskschedulerschema-timetrigger-triggergroup-element.md)                             | [<span data-ttu-id="3f918-132">**timeTriggerType**</span><span class="sxs-lookup"><span data-stu-id="3f918-132">**timeTriggerType**</span></span>](taskschedulerschema-timetriggertype-complextype.md)                             | <span data-ttu-id="3f918-133">啟動觸發程式時啟動工作的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="3f918-133">A trigger that starts a task when the trigger is activated.</span></span><br/>                                            |



## <a name="remarks"></a><span data-ttu-id="3f918-134">備註</span><span class="sxs-lookup"><span data-stu-id="3f918-134">Remarks</span></span>

<span data-ttu-id="3f918-135">讀取或寫入 XML 時，此群組所定義的元素是 [**觸發**](taskschedulerschema-triggers-tasktype-element.md) 程式元素的子項目。</span><span class="sxs-lookup"><span data-stu-id="3f918-135">When reading or writing XML, the elements that are defined by this group are the child elements of the [**Triggers**](taskschedulerschema-triggers-tasktype-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f918-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="3f918-136">Requirements</span></span>



| <span data-ttu-id="3f918-137">需求</span><span class="sxs-lookup"><span data-stu-id="3f918-137">Requirement</span></span> | <span data-ttu-id="3f918-138">值</span><span class="sxs-lookup"><span data-stu-id="3f918-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3f918-139">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3f918-139">Minimum supported client</span></span><br/> | <span data-ttu-id="3f918-140">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3f918-140">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="3f918-141">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3f918-141">Minimum supported server</span></span><br/> | <span data-ttu-id="3f918-142">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3f918-142">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3f918-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3f918-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f918-144">工作排程器</span><span class="sxs-lookup"><span data-stu-id="3f918-144">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





