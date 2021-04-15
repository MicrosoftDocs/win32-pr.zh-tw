---
title: 重複 (triggerBaseType) 元素
description: 指定執行工作的頻率，以及啟動工作之後重複模式重複的時間長度。
ms.assetid: d43c7f9a-3a7b-44a9-901b-9ad18c027b1b
keywords:
- 重複元素工作排程器
topic_type:
- apiref
api_name:
- Repetition
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7ebd6f9f77998e5e975e24ff752a475e3880c0aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466016"
---
# <a name="repetition-triggerbasetype-element"></a><span data-ttu-id="fcb2b-104">重複 (triggerBaseType) 元素</span><span class="sxs-lookup"><span data-stu-id="fcb2b-104">Repetition (triggerBaseType) Element</span></span>

<span data-ttu-id="fcb2b-105">指定執行工作的頻率，以及啟動工作之後重複模式重複的時間長度。</span><span class="sxs-lookup"><span data-stu-id="fcb2b-105">Specifies how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span>

``` syntax
<xs:element name="Repetition"
    type="repetitionType"
 />
```

<span data-ttu-id="fcb2b-106">**重複** 專案是由 [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="fcb2b-106">The **Repetition** element is defined by the [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="fcb2b-107">父元素</span><span class="sxs-lookup"><span data-stu-id="fcb2b-107">Parent element</span></span>



| <span data-ttu-id="fcb2b-108">元素</span><span class="sxs-lookup"><span data-stu-id="fcb2b-108">Element</span></span>                                                                                     | <span data-ttu-id="fcb2b-109">衍生自</span><span class="sxs-lookup"><span data-stu-id="fcb2b-109">Derived from</span></span>                                                                               | <span data-ttu-id="fcb2b-110">Description</span><span class="sxs-lookup"><span data-stu-id="fcb2b-110">Description</span></span>                                                                                  |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fcb2b-111">**BootTrigger**</span><span class="sxs-lookup"><span data-stu-id="fcb2b-111">**BootTrigger**</span></span>](taskschedulerschema-boottrigger-triggergroup-element.md)                 | [<span data-ttu-id="fcb2b-112">**bootTriggerType**</span><span class="sxs-lookup"><span data-stu-id="fcb2b-112">**bootTriggerType**</span></span>](taskschedulerschema-boottriggertype-complextype.md)                 | <span data-ttu-id="fcb2b-113">指定啟動系統時啟動工作的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="fcb2b-113">Specifies a trigger that starts a task when the system is booted.</span></span><br/>                 |
| [<span data-ttu-id="fcb2b-114">**CalendarTrigger**</span><span class="sxs-lookup"><span data-stu-id="fcb2b-114">**CalendarTrigger**</span></span>](taskschedulerschema-calendartrigger-triggergroup-element.md)         | [<span data-ttu-id="fcb2b-115">**calendarTriggerType**</span><span class="sxs-lookup"><span data-stu-id="fcb2b-115">**calendarTriggerType**</span></span>](taskschedulerschema-calendartriggertype-complextype.md)         | <span data-ttu-id="fcb2b-116">指定每日、每週、每月或每週 (DOW) 觸發程式。</span><span class="sxs-lookup"><span data-stu-id="fcb2b-116">Specifies a daily, weekly, monthly, or a monthly day-of-the-week (DOW) trigger.</span></span><br/>   |
| [<span data-ttu-id="fcb2b-117">**EventTrigger**</span><span class="sxs-lookup"><span data-stu-id="fcb2b-117">**EventTrigger**</span></span>](taskschedulerschema-eventtrigger-triggergroup-element.md)               | [<span data-ttu-id="fcb2b-118">**eventTriggerType**</span><span class="sxs-lookup"><span data-stu-id="fcb2b-118">**eventTriggerType**</span></span>](taskschedulerschema-eventtriggertype-complextype.md)               | <span data-ttu-id="fcb2b-119">指定在發生系統事件時啟動工作的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="fcb2b-119">Specifies a trigger that starts a task when a system event occurs.</span></span><br/>                |
| [<span data-ttu-id="fcb2b-120">**IdleTrigger**</span><span class="sxs-lookup"><span data-stu-id="fcb2b-120">**IdleTrigger**</span></span>](taskschedulerschema-idletrigger-triggergroup-element.md)                 | [<span data-ttu-id="fcb2b-121">**idleTriggerType**</span><span class="sxs-lookup"><span data-stu-id="fcb2b-121">**idleTriggerType**</span></span>](taskschedulerschema-idletriggertype-complextype.md)                 | <span data-ttu-id="fcb2b-122">指定當電腦進入閒置狀態時啟動工作的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="fcb2b-122">Specifies a trigger that starts a task when the computer goes into an idle state.</span></span><br/> |
| [<span data-ttu-id="fcb2b-123">**LogonTrigger**</span><span class="sxs-lookup"><span data-stu-id="fcb2b-123">**LogonTrigger**</span></span>](taskschedulerschema-logontrigger-triggergroup-element.md)               | [<span data-ttu-id="fcb2b-124">**logonTriggerType**</span><span class="sxs-lookup"><span data-stu-id="fcb2b-124">**logonTriggerType**</span></span>](taskschedulerschema-logontriggertype-complextype.md)               | <span data-ttu-id="fcb2b-125">指定當使用者登入時啟動工作的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="fcb2b-125">Specifies a trigger that starts a task when a user logs on.</span></span><br/>                       |
| [<span data-ttu-id="fcb2b-126">**RegistrationTrigger**</span><span class="sxs-lookup"><span data-stu-id="fcb2b-126">**RegistrationTrigger**</span></span>](taskschedulerschema-registrationtrigger-triggergroup-element.md) | [<span data-ttu-id="fcb2b-127">**registrationTriggerType**</span><span class="sxs-lookup"><span data-stu-id="fcb2b-127">**registrationTriggerType**</span></span>](taskschedulerschema-registrationtriggertype-complextype.md) | <span data-ttu-id="fcb2b-128">指定在註冊工作時啟動工作的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="fcb2b-128">Specifies a trigger that starts a task when the task is registered.</span></span><br/>               |
| [<span data-ttu-id="fcb2b-129">**TimeTrigger**</span><span class="sxs-lookup"><span data-stu-id="fcb2b-129">**TimeTrigger**</span></span>](taskschedulerschema-timetrigger-triggergroup-element.md)                 | [<span data-ttu-id="fcb2b-130">**timeTriggerType**</span><span class="sxs-lookup"><span data-stu-id="fcb2b-130">**timeTriggerType**</span></span>](taskschedulerschema-timetriggertype-complextype.md)                 | <span data-ttu-id="fcb2b-131">指定啟動觸發程式時啟動工作的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="fcb2b-131">Specifies a trigger that starts a task when the trigger is activated.</span></span><br/>             |



## <a name="child-elements"></a><span data-ttu-id="fcb2b-132">子元素</span><span class="sxs-lookup"><span data-stu-id="fcb2b-132">Child elements</span></span>



| <span data-ttu-id="fcb2b-133">元素</span><span class="sxs-lookup"><span data-stu-id="fcb2b-133">Element</span></span>                                                                                   | <span data-ttu-id="fcb2b-134">類型</span><span class="sxs-lookup"><span data-stu-id="fcb2b-134">Type</span></span>     | <span data-ttu-id="fcb2b-135">Description</span><span class="sxs-lookup"><span data-stu-id="fcb2b-135">Description</span></span>                                                                                                         |
|-------------------------------------------------------------------------------------------|----------|---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fcb2b-136">**時間**</span><span class="sxs-lookup"><span data-stu-id="fcb2b-136">**Duration**</span></span>](taskschedulerschema-duration-repetitiontype-element.md)                   | <span data-ttu-id="fcb2b-137">duration</span><span class="sxs-lookup"><span data-stu-id="fcb2b-137">duration</span></span> | <span data-ttu-id="fcb2b-138">指定重複模式的時間長度。</span><span class="sxs-lookup"><span data-stu-id="fcb2b-138">Specifies how long the pattern is repeated.</span></span><br/>                                                              |
| [<span data-ttu-id="fcb2b-139">**間隔**</span><span class="sxs-lookup"><span data-stu-id="fcb2b-139">**Interval**</span></span>](taskschedulerschema-interval-repetitiontype-element.md)                   | <span data-ttu-id="fcb2b-140">duration</span><span class="sxs-lookup"><span data-stu-id="fcb2b-140">duration</span></span> | <span data-ttu-id="fcb2b-141">指定工作每次重新開機之間的時間量。</span><span class="sxs-lookup"><span data-stu-id="fcb2b-141">Specifies the amount of time between each restart of the task.</span></span><br/>                                           |
| [<span data-ttu-id="fcb2b-142">**StopAtDurationEnd**</span><span class="sxs-lookup"><span data-stu-id="fcb2b-142">**StopAtDurationEnd**</span></span>](taskschedulerschema-stopatdurationend-repetitiontype-element.md) | <span data-ttu-id="fcb2b-143">boolean</span><span class="sxs-lookup"><span data-stu-id="fcb2b-143">boolean</span></span>  | <span data-ttu-id="fcb2b-144">指定在重複模式期間結束時停止執行中的工作實例。</span><span class="sxs-lookup"><span data-stu-id="fcb2b-144">Specifies that a running instances of the task is stopped at the end of the repetition pattern duration.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="fcb2b-145">備註</span><span class="sxs-lookup"><span data-stu-id="fcb2b-145">Remarks</span></span>

<span data-ttu-id="fcb2b-146">如果您指定工作的重複持續時間，您也必須指定重複間隔。</span><span class="sxs-lookup"><span data-stu-id="fcb2b-146">If you specify a repetition duration for a task, you must also specify the repetition interval.</span></span>

<span data-ttu-id="fcb2b-147">如果您註冊的工作包含重複間隔等於1分鐘的觸發程式，且重複持續時間等於四分鐘，則工作會啟動五次。</span><span class="sxs-lookup"><span data-stu-id="fcb2b-147">If you register a task that contains a trigger with a repetition interval equal to one minute and a repetition duration equal to four minutes, the task will be launched five times.</span></span> <span data-ttu-id="fcb2b-148">您可以使用下列模式來定義五次重複。</span><span class="sxs-lookup"><span data-stu-id="fcb2b-148">The five repetitions can be defined by the following pattern.</span></span>

1.  <span data-ttu-id="fcb2b-149">工作會在第一分鐘的開頭開始。</span><span class="sxs-lookup"><span data-stu-id="fcb2b-149">A task starts at the beginning of the first minute.</span></span>
2.  <span data-ttu-id="fcb2b-150">下一項工作會在第一分鐘結束時啟動。</span><span class="sxs-lookup"><span data-stu-id="fcb2b-150">The next task starts at the end of the first minute.</span></span>
3.  <span data-ttu-id="fcb2b-151">下一項工作會在第二分鐘結束時啟動。</span><span class="sxs-lookup"><span data-stu-id="fcb2b-151">The next task starts at the end of the second minute.</span></span>
4.  <span data-ttu-id="fcb2b-152">下一項工作會從第三分鐘的結尾開始。</span><span class="sxs-lookup"><span data-stu-id="fcb2b-152">The next task starts at the end of the third minute.</span></span>
5.  <span data-ttu-id="fcb2b-153">下一項工作會在第四分鐘結束時啟動。</span><span class="sxs-lookup"><span data-stu-id="fcb2b-153">The next task starts at the end of the fourth minute.</span></span>

<span data-ttu-id="fcb2b-154">**Windows Server 2003、WINDOWS XP 和 windows 2000：** 如果您註冊的工作包含重複間隔等於1分鐘的觸發程式，且重複持續時間等於四分鐘，則工作會啟動四次。</span><span class="sxs-lookup"><span data-stu-id="fcb2b-154">**Windows Server 2003, Windows XP and Windows 2000:** If you register a task that contains a trigger with a repetition interval equal to one minute and a repetition duration equal to four minutes, the task will be launched four times.</span></span>

<span data-ttu-id="fcb2b-155">**Windows Vista、windows 7、Windows server 2008、Windows 8 和 Windows server 2012：** 通常，將重複期間設定為間隔的確切倍數，會產生上面所述的數位。</span><span class="sxs-lookup"><span data-stu-id="fcb2b-155">**Windows Vista, Windows 7, Windows Server 2008, Windows 8 and Windows Server 2012:** Usually, setting the repetition duration to an exact multiple of the interval yields the numbers described above.</span></span> <span data-ttu-id="fcb2b-156">不過，在某些繁重的負載狀況下，可能會在 TaskScheduler 可以啟動最後工作間隔之前，讓持續時間超時。</span><span class="sxs-lookup"><span data-stu-id="fcb2b-156">However, under certain heavy load conditions, it is possible for the duration to timeout before TaskScheduler can launch the final task interval.</span></span>

<span data-ttu-id="fcb2b-157">針對開發腳本，會使用觸發程式來指定重複模式。所有觸發程式物件都會繼承 [**重複**](trigger-repetition.md) 的屬性。</span><span class="sxs-lookup"><span data-stu-id="fcb2b-157">For scripting development, the repetition pattern is specified using the [**Trigger.Repetition**](trigger-repetition.md) property that is inherited by all the trigger objects.</span></span>

<span data-ttu-id="fcb2b-158">若是 c + + 開發，則會使用所有觸發程式介面所繼承的 [**ITRigger：：重複**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_repetition) 屬性來指定重複模式。</span><span class="sxs-lookup"><span data-stu-id="fcb2b-158">For C++ development, the repetition pattern is specified using the [**ITRigger::Repetition**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_repetition) property that is inherited by all the trigger interfaces.</span></span>

## <a name="examples"></a><span data-ttu-id="fcb2b-159">範例</span><span class="sxs-lookup"><span data-stu-id="fcb2b-159">Examples</span></span>

<span data-ttu-id="fcb2b-160">下列 XML 會定義一個開機觸發程式元素，以指定觸發程式的重複模式。</span><span class="sxs-lookup"><span data-stu-id="fcb2b-160">The following XML defines a boot trigger element that specifies a repetition pattern for a trigger.</span></span>


```XML
<BootTrigger>
    <StartBoundary>2005-01-01T08:00:00</StartBoundary>
    <EndBounadry>2007-01-01T08:00:00</EndBoundary>
    <Enabled>true</Enabled>
    <Repetition>
        <Interval></Interval>
        <Duration></Duration>
        <StopAtDurationEnd>true</StopAtDirationEnd>
    </Repetition>
    <ExecutionTimeLimit></ExecutionTimeLimit>
    <Delay><Delay>
 </BootTrigger>
```



## <a name="requirements"></a><span data-ttu-id="fcb2b-161">規格需求</span><span class="sxs-lookup"><span data-stu-id="fcb2b-161">Requirements</span></span>



| <span data-ttu-id="fcb2b-162">需求</span><span class="sxs-lookup"><span data-stu-id="fcb2b-162">Requirement</span></span> | <span data-ttu-id="fcb2b-163">值</span><span class="sxs-lookup"><span data-stu-id="fcb2b-163">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="fcb2b-164">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fcb2b-164">Minimum supported client</span></span><br/> | <span data-ttu-id="fcb2b-165">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fcb2b-165">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="fcb2b-166">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fcb2b-166">Minimum supported server</span></span><br/> | <span data-ttu-id="fcb2b-167">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fcb2b-167">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fcb2b-168">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fcb2b-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fcb2b-169">工作排程器架構元素</span><span class="sxs-lookup"><span data-stu-id="fcb2b-169">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="fcb2b-170">工作排程器</span><span class="sxs-lookup"><span data-stu-id="fcb2b-170">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





