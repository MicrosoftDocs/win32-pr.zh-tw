---
title: EndBoundary (triggerBaseType) 元素
description: 指定停用觸發程式的日期和時間。 觸發程式在停用之後無法啟動工作。
ms.assetid: 84731c0b-3fb8-44dd-be1a-67547add1f9e
keywords:
- EndBoundary 元素工作排程器
topic_type:
- apiref
api_name:
- EndBoundary
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d687655498301595c1ab888fcc179ec0694f0aef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969757"
---
# <a name="endboundary-triggerbasetype-element"></a><span data-ttu-id="07ba2-105">EndBoundary (triggerBaseType) 元素</span><span class="sxs-lookup"><span data-stu-id="07ba2-105">EndBoundary (triggerBaseType) Element</span></span>

<span data-ttu-id="07ba2-106">指定停用觸發程式的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="07ba2-106">Specifies the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="07ba2-107">觸發程式在停用之後無法啟動工作。</span><span class="sxs-lookup"><span data-stu-id="07ba2-107">The trigger cannot start the task after it is deactivated.</span></span>

``` syntax
<xs:element name="EndBoundary"
    type="dateTime"
 />
```

<span data-ttu-id="07ba2-108">**EndBoundary** 元素是由 [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="07ba2-108">The **EndBoundary** element is defined by the [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="07ba2-109">父元素</span><span class="sxs-lookup"><span data-stu-id="07ba2-109">Parent element</span></span>



| <span data-ttu-id="07ba2-110">元素</span><span class="sxs-lookup"><span data-stu-id="07ba2-110">Element</span></span>                                                                                     | <span data-ttu-id="07ba2-111">衍生自</span><span class="sxs-lookup"><span data-stu-id="07ba2-111">Derived from</span></span>                                                                               | <span data-ttu-id="07ba2-112">Description</span><span class="sxs-lookup"><span data-stu-id="07ba2-112">Description</span></span>                                                                                  |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="07ba2-113">**BootTrigger**</span><span class="sxs-lookup"><span data-stu-id="07ba2-113">**BootTrigger**</span></span>](taskschedulerschema-boottrigger-triggergroup-element.md)                 | [<span data-ttu-id="07ba2-114">**bootTriggerType**</span><span class="sxs-lookup"><span data-stu-id="07ba2-114">**bootTriggerType**</span></span>](taskschedulerschema-boottriggertype-complextype.md)                 | <span data-ttu-id="07ba2-115">指定啟動系統時啟動工作的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="07ba2-115">Specifies a trigger that starts a task when the system is booted.</span></span><br/>                 |
| [<span data-ttu-id="07ba2-116">**CalendarTrigger**</span><span class="sxs-lookup"><span data-stu-id="07ba2-116">**CalendarTrigger**</span></span>](taskschedulerschema-calendartrigger-triggergroup-element.md)         | [<span data-ttu-id="07ba2-117">**calendarTriggerType**</span><span class="sxs-lookup"><span data-stu-id="07ba2-117">**calendarTriggerType**</span></span>](taskschedulerschema-calendartriggertype-complextype.md)         | <span data-ttu-id="07ba2-118">指定每日、每週、每月或每週 (DOW) 觸發程式。</span><span class="sxs-lookup"><span data-stu-id="07ba2-118">Specifies a daily, weekly, monthly, or a monthly day-of-the-week (DOW) trigger.</span></span><br/>   |
| [<span data-ttu-id="07ba2-119">**EventTrigger**</span><span class="sxs-lookup"><span data-stu-id="07ba2-119">**EventTrigger**</span></span>](taskschedulerschema-eventtrigger-triggergroup-element.md)               | [<span data-ttu-id="07ba2-120">**eventTriggerType**</span><span class="sxs-lookup"><span data-stu-id="07ba2-120">**eventTriggerType**</span></span>](taskschedulerschema-eventtriggertype-complextype.md)               | <span data-ttu-id="07ba2-121">指定在發生系統事件時啟動工作的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="07ba2-121">Specifies a trigger that starts a task when a system event occurs.</span></span><br/>                |
| [<span data-ttu-id="07ba2-122">**IdleTrigger**</span><span class="sxs-lookup"><span data-stu-id="07ba2-122">**IdleTrigger**</span></span>](taskschedulerschema-idletrigger-triggergroup-element.md)                 | [<span data-ttu-id="07ba2-123">**idleTriggerType**</span><span class="sxs-lookup"><span data-stu-id="07ba2-123">**idleTriggerType**</span></span>](taskschedulerschema-idletriggertype-complextype.md)                 | <span data-ttu-id="07ba2-124">指定當電腦進入閒置狀態時啟動工作的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="07ba2-124">Specifies a trigger that starts a task when the computer goes into an idle state.</span></span><br/> |
| [<span data-ttu-id="07ba2-125">**LogonTrigger**</span><span class="sxs-lookup"><span data-stu-id="07ba2-125">**LogonTrigger**</span></span>](taskschedulerschema-logontrigger-triggergroup-element.md)               | [<span data-ttu-id="07ba2-126">**logonTriggerType**</span><span class="sxs-lookup"><span data-stu-id="07ba2-126">**logonTriggerType**</span></span>](taskschedulerschema-logontriggertype-complextype.md)               | <span data-ttu-id="07ba2-127">指定當使用者登入時啟動工作的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="07ba2-127">Specifies a trigger that starts a task when a user logs on.</span></span><br/>                       |
| [<span data-ttu-id="07ba2-128">**RegistrationTrigger**</span><span class="sxs-lookup"><span data-stu-id="07ba2-128">**RegistrationTrigger**</span></span>](taskschedulerschema-registrationtrigger-triggergroup-element.md) | [<span data-ttu-id="07ba2-129">**registrationTriggerType**</span><span class="sxs-lookup"><span data-stu-id="07ba2-129">**registrationTriggerType**</span></span>](taskschedulerschema-registrationtriggertype-complextype.md) | <span data-ttu-id="07ba2-130">指定在註冊工作時啟動工作的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="07ba2-130">Specifies a trigger that starts a task when the task is registered.</span></span><br/>               |
| [<span data-ttu-id="07ba2-131">**TimeTrigger**</span><span class="sxs-lookup"><span data-stu-id="07ba2-131">**TimeTrigger**</span></span>](taskschedulerschema-timetrigger-triggergroup-element.md)                 | [<span data-ttu-id="07ba2-132">**timeTriggerType**</span><span class="sxs-lookup"><span data-stu-id="07ba2-132">**timeTriggerType**</span></span>](taskschedulerschema-timetriggertype-complextype.md)                 | <span data-ttu-id="07ba2-133">指定啟動觸發程式時啟動工作的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="07ba2-133">Specifies a trigger that starts a task when the trigger is activated.</span></span><br/>             |



## <a name="remarks"></a><span data-ttu-id="07ba2-134">備註</span><span class="sxs-lookup"><span data-stu-id="07ba2-134">Remarks</span></span>

<span data-ttu-id="07ba2-135">針對開發腳本，會使用所有觸發程式物件所繼承的 [**EndBoundary**](trigger-endboundary.md) 屬性來指定結束界限。</span><span class="sxs-lookup"><span data-stu-id="07ba2-135">For scripting development, the end boundary is specified using the [**Trigger.EndBoundary**](trigger-endboundary.md) property that is inherited by the all trigger objects.</span></span>

<span data-ttu-id="07ba2-136">若是 c + + 開發，則會使用所有觸發程式介面所繼承的 [**ITrigger：： EndBoundary**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_endboundary) 屬性來指定結束界限。</span><span class="sxs-lookup"><span data-stu-id="07ba2-136">For C++ development, the end boundary is specified using the [**ITrigger::EndBoundary**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_endboundary) property that is inherited by the all trigger interfaces.</span></span>

## <a name="examples"></a><span data-ttu-id="07ba2-137">範例</span><span class="sxs-lookup"><span data-stu-id="07ba2-137">Examples</span></span>

<span data-ttu-id="07ba2-138">下列 XML 定義的開機觸發程式元素，定義2007年1月1日的結束界限： 8:00 AM。</span><span class="sxs-lookup"><span data-stu-id="07ba2-138">The following XML defines a boot trigger element that defines an end boundary of January 1, 2007: 8:00 AM.</span></span>


```XML
<BootTrigger>
    <StartBoundary>2005-01-01T08:00:00</StartBoundary>
    <EndBounadry>2007-01-01T08:00:00</EndBoundary>
    <Enabled>true</Enabled>
    <Repetition></Repetition>
    <ExecutionTimeLimit></ExecutionTimeLimit>
    <Delay><Delay>
 </BootTrigger>
```



## <a name="requirements"></a><span data-ttu-id="07ba2-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="07ba2-139">Requirements</span></span>



| <span data-ttu-id="07ba2-140">需求</span><span class="sxs-lookup"><span data-stu-id="07ba2-140">Requirement</span></span> | <span data-ttu-id="07ba2-141">值</span><span class="sxs-lookup"><span data-stu-id="07ba2-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="07ba2-142">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="07ba2-142">Minimum supported client</span></span><br/> | <span data-ttu-id="07ba2-143">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="07ba2-143">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="07ba2-144">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="07ba2-144">Minimum supported server</span></span><br/> | <span data-ttu-id="07ba2-145">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="07ba2-145">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="07ba2-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="07ba2-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07ba2-147">工作排程器架構元素</span><span class="sxs-lookup"><span data-stu-id="07ba2-147">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="07ba2-148">工作排程器</span><span class="sxs-lookup"><span data-stu-id="07ba2-148">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





