---
title: StartBoundary (triggerBaseType) 元素
description: 指定啟動觸發程式的日期和時間。
ms.assetid: 95a62ae5-4eba-49df-a25f-0d1181772833
keywords:
- StartBoundary 元素工作排程器
topic_type:
- apiref
api_name:
- StartBoundary
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8d6adf90de2f3b199f98737996fe732f342787b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094131"
---
# <a name="startboundary-triggerbasetype-element"></a><span data-ttu-id="8bc34-104">StartBoundary (triggerBaseType) 元素</span><span class="sxs-lookup"><span data-stu-id="8bc34-104">StartBoundary (triggerBaseType) Element</span></span>

<span data-ttu-id="8bc34-105">指定啟動觸發程式的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="8bc34-105">Specifies the date and time when the trigger is activated.</span></span>

``` syntax
<xs:element name="StartBoundary"
    type="dateTime"
 />
```

<span data-ttu-id="8bc34-106">**StartBoundary** 元素是由 [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="8bc34-106">The **StartBoundary** element is defined by the [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="8bc34-107">父元素</span><span class="sxs-lookup"><span data-stu-id="8bc34-107">Parent element</span></span>



| <span data-ttu-id="8bc34-108">元素</span><span class="sxs-lookup"><span data-stu-id="8bc34-108">Element</span></span>                                                                                     | <span data-ttu-id="8bc34-109">衍生自</span><span class="sxs-lookup"><span data-stu-id="8bc34-109">Derived from</span></span>                                                                               | <span data-ttu-id="8bc34-110">Description</span><span class="sxs-lookup"><span data-stu-id="8bc34-110">Description</span></span>                                                                                  |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8bc34-111">**BootTrigger**</span><span class="sxs-lookup"><span data-stu-id="8bc34-111">**BootTrigger**</span></span>](taskschedulerschema-boottrigger-triggergroup-element.md)                 | [<span data-ttu-id="8bc34-112">**bootTriggerType**</span><span class="sxs-lookup"><span data-stu-id="8bc34-112">**bootTriggerType**</span></span>](taskschedulerschema-boottriggertype-complextype.md)                 | <span data-ttu-id="8bc34-113">指定啟動系統時啟動工作的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="8bc34-113">Specifies a trigger that starts a task when the system is booted.</span></span><br/>                 |
| [<span data-ttu-id="8bc34-114">**CalendarTrigger**</span><span class="sxs-lookup"><span data-stu-id="8bc34-114">**CalendarTrigger**</span></span>](taskschedulerschema-calendartrigger-triggergroup-element.md)         | [<span data-ttu-id="8bc34-115">**calendarTriggerType**</span><span class="sxs-lookup"><span data-stu-id="8bc34-115">**calendarTriggerType**</span></span>](taskschedulerschema-calendartriggertype-complextype.md)         | <span data-ttu-id="8bc34-116">指定每日、每週、每月或每週 (DOW) 觸發程式。</span><span class="sxs-lookup"><span data-stu-id="8bc34-116">Specifies a daily, weekly, monthly, or a monthly day-of-the-week (DOW) trigger.</span></span><br/>   |
| [<span data-ttu-id="8bc34-117">**EventTrigger**</span><span class="sxs-lookup"><span data-stu-id="8bc34-117">**EventTrigger**</span></span>](taskschedulerschema-eventtrigger-triggergroup-element.md)               | [<span data-ttu-id="8bc34-118">**eventTriggerType**</span><span class="sxs-lookup"><span data-stu-id="8bc34-118">**eventTriggerType**</span></span>](taskschedulerschema-eventtriggertype-complextype.md)               | <span data-ttu-id="8bc34-119">指定在發生系統事件時啟動工作的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="8bc34-119">Specifies a trigger that starts a task when a system event occurs.</span></span><br/>                |
| [<span data-ttu-id="8bc34-120">**IdleTrigger**</span><span class="sxs-lookup"><span data-stu-id="8bc34-120">**IdleTrigger**</span></span>](taskschedulerschema-idletrigger-triggergroup-element.md)                 | [<span data-ttu-id="8bc34-121">**idleTriggerType**</span><span class="sxs-lookup"><span data-stu-id="8bc34-121">**idleTriggerType**</span></span>](taskschedulerschema-idletriggertype-complextype.md)                 | <span data-ttu-id="8bc34-122">指定當電腦進入閒置狀態時啟動工作的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="8bc34-122">Specifies a trigger that starts a task when the computer goes into an idle state.</span></span><br/> |
| [<span data-ttu-id="8bc34-123">**LogonTrigger**</span><span class="sxs-lookup"><span data-stu-id="8bc34-123">**LogonTrigger**</span></span>](taskschedulerschema-logontrigger-triggergroup-element.md)               | [<span data-ttu-id="8bc34-124">**logonTriggerType**</span><span class="sxs-lookup"><span data-stu-id="8bc34-124">**logonTriggerType**</span></span>](taskschedulerschema-logontriggertype-complextype.md)               | <span data-ttu-id="8bc34-125">指定當使用者登入時啟動工作的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="8bc34-125">Specifies a trigger that starts a task when a user logs on.</span></span><br/>                       |
| [<span data-ttu-id="8bc34-126">**RegistrationTrigger**</span><span class="sxs-lookup"><span data-stu-id="8bc34-126">**RegistrationTrigger**</span></span>](taskschedulerschema-registrationtrigger-triggergroup-element.md) | [<span data-ttu-id="8bc34-127">**registrationTriggerType**</span><span class="sxs-lookup"><span data-stu-id="8bc34-127">**registrationTriggerType**</span></span>](taskschedulerschema-registrationtriggertype-complextype.md) | <span data-ttu-id="8bc34-128">指定在註冊工作時啟動工作的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="8bc34-128">Specifies a trigger that starts a task when the task is registered.</span></span><br/>               |
| [<span data-ttu-id="8bc34-129">**TimeTrigger**</span><span class="sxs-lookup"><span data-stu-id="8bc34-129">**TimeTrigger**</span></span>](taskschedulerschema-timetrigger-triggergroup-element.md)                 | [<span data-ttu-id="8bc34-130">**timeTriggerType**</span><span class="sxs-lookup"><span data-stu-id="8bc34-130">**timeTriggerType**</span></span>](taskschedulerschema-timetriggertype-complextype.md)                 | <span data-ttu-id="8bc34-131">指定啟動觸發程式時啟動工作的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="8bc34-131">Specifies a trigger that starts a task when the trigger is activated.</span></span><br/>             |



## <a name="remarks"></a><span data-ttu-id="8bc34-132">備註</span><span class="sxs-lookup"><span data-stu-id="8bc34-132">Remarks</span></span>

<span data-ttu-id="8bc34-133">專案 **<StartBoundary>** 是時間和行事曆觸發程式 (和) 的必要元素 [**<TimeTrigger>**](taskschedulerschema-timetrigger-triggergroup-element.md) [**<CalendarTrigger>**](taskschedulerschema-calendartrigger-triggergroup-element.md) 。</span><span class="sxs-lookup"><span data-stu-id="8bc34-133">The **<StartBoundary>** element is a required element for time and calendar triggers ([**<TimeTrigger>**](taskschedulerschema-timetrigger-triggergroup-element.md) and [**<CalendarTrigger>**](taskschedulerschema-calendartrigger-triggergroup-element.md)).</span></span>

<span data-ttu-id="8bc34-134">針對開發腳本，會使用所有觸發程式物件所繼承的 [**StartBoundary**](trigger-startboundary.md) 屬性來指定結束界限。</span><span class="sxs-lookup"><span data-stu-id="8bc34-134">For scripting development, the end boundary is specified using the [**Trigger.StartBoundary**](trigger-startboundary.md) property that is inherited by the all trigger objects.</span></span>

<span data-ttu-id="8bc34-135">若是 c + + 開發，則會使用所有觸發程式介面所繼承的 [**ITrigger：： StartBoundary**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_startboundary) 屬性來指定結束界限。</span><span class="sxs-lookup"><span data-stu-id="8bc34-135">For C++ development, the end boundary is specified using the [**ITrigger::StartBoundary**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_startboundary) property that is inherited by the all trigger interfaces.</span></span>

## <a name="examples"></a><span data-ttu-id="8bc34-136">範例</span><span class="sxs-lookup"><span data-stu-id="8bc34-136">Examples</span></span>

<span data-ttu-id="8bc34-137">下列 XML 定義的開機觸發程式元素會定義2005年1月1日的起始界限： 8:00 AM。</span><span class="sxs-lookup"><span data-stu-id="8bc34-137">The following XML defines a boot trigger element that defines a start boundary of January 1, 2005: 8:00 AM.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="8bc34-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="8bc34-138">Requirements</span></span>



| <span data-ttu-id="8bc34-139">需求</span><span class="sxs-lookup"><span data-stu-id="8bc34-139">Requirement</span></span> | <span data-ttu-id="8bc34-140">值</span><span class="sxs-lookup"><span data-stu-id="8bc34-140">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="8bc34-141">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8bc34-141">Minimum supported client</span></span><br/> | <span data-ttu-id="8bc34-142">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8bc34-142">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="8bc34-143">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8bc34-143">Minimum supported server</span></span><br/> | <span data-ttu-id="8bc34-144">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8bc34-144">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8bc34-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8bc34-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8bc34-146">工作排程器架構元素</span><span class="sxs-lookup"><span data-stu-id="8bc34-146">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="8bc34-147">工作排程器</span><span class="sxs-lookup"><span data-stu-id="8bc34-147">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





