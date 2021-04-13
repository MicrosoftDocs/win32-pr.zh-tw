---
title: ExecutionTimeLimit (triggerBaseType) 元素
description: 指定觸發程式可啟動工作的最大時間量。
ms.assetid: f78e7c7b-d069-4920-9435-020f6e081eff
keywords:
- ExecutionTimeLimit 元素工作排程器
topic_type:
- apiref
api_name:
- ExecutionTimeLimit
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fbe56fb0431ab109b1a19030ae6ba20af55492ea
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466285"
---
# <a name="executiontimelimit-triggerbasetype-element"></a><span data-ttu-id="bbcd0-104">ExecutionTimeLimit (triggerBaseType) 元素</span><span class="sxs-lookup"><span data-stu-id="bbcd0-104">ExecutionTimeLimit (triggerBaseType) Element</span></span>

<span data-ttu-id="bbcd0-105">指定觸發程式可啟動工作的最大時間量。</span><span class="sxs-lookup"><span data-stu-id="bbcd0-105">Specifies the maximum amount of time in which the task can be started by the trigger.</span></span> <span data-ttu-id="bbcd0-106">此字串的格式為 PnYnMnDTnHnMnS，其中 nY 是年數，nM 是月數，nD 是天數、t ' 是日期/時間分隔符號、nH 是時數、nM 為分鐘數，而 nS 是以秒為單位的秒數，例如，PT5M 指定 (5 分鐘，P1M4DT2H5M 指定一個月、四天、兩小時和五分鐘的) 。</span><span class="sxs-lookup"><span data-stu-id="bbcd0-106">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="bbcd0-107">如需持續時間類型的詳細資訊，請參閱 <https://go.microsoft.com/fwlink/p/?linkid=106886> 。</span><span class="sxs-lookup"><span data-stu-id="bbcd0-107">For more information about the duration type, see <https://go.microsoft.com/fwlink/p/?linkid=106886>.</span></span>

``` syntax
<xs:element name="ExecutionTimeLimit"
    type="duration"
 />
```

<span data-ttu-id="bbcd0-108">**ExecutionTimeLimit** 元素是由 [**triggerBaseType**](taskschedulerschema-boottriggertype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="bbcd0-108">The **ExecutionTimeLimit** element is defined by the [**triggerBaseType**](taskschedulerschema-boottriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="bbcd0-109">父元素</span><span class="sxs-lookup"><span data-stu-id="bbcd0-109">Parent element</span></span>



| <span data-ttu-id="bbcd0-110">元素</span><span class="sxs-lookup"><span data-stu-id="bbcd0-110">Element</span></span>                                                                                     | <span data-ttu-id="bbcd0-111">衍生自</span><span class="sxs-lookup"><span data-stu-id="bbcd0-111">Derived from</span></span>                                                                               | <span data-ttu-id="bbcd0-112">Description</span><span class="sxs-lookup"><span data-stu-id="bbcd0-112">Description</span></span>                                                                                  |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bbcd0-113">**BootTrigger**</span><span class="sxs-lookup"><span data-stu-id="bbcd0-113">**BootTrigger**</span></span>](taskschedulerschema-boottrigger-triggergroup-element.md)                 | [<span data-ttu-id="bbcd0-114">**bootTriggerType**</span><span class="sxs-lookup"><span data-stu-id="bbcd0-114">**bootTriggerType**</span></span>](taskschedulerschema-boottriggertype-complextype.md)                 | <span data-ttu-id="bbcd0-115">指定啟動系統時啟動工作的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="bbcd0-115">Specifies a trigger that starts a task when the system is booted.</span></span><br/>                 |
| [<span data-ttu-id="bbcd0-116">**CalendarTrigger**</span><span class="sxs-lookup"><span data-stu-id="bbcd0-116">**CalendarTrigger**</span></span>](taskschedulerschema-calendartrigger-triggergroup-element.md)         | [<span data-ttu-id="bbcd0-117">**calendarTriggerType**</span><span class="sxs-lookup"><span data-stu-id="bbcd0-117">**calendarTriggerType**</span></span>](taskschedulerschema-calendartriggertype-complextype.md)         | <span data-ttu-id="bbcd0-118">指定每日、每週、每月或每週 (DOW) 觸發程式。</span><span class="sxs-lookup"><span data-stu-id="bbcd0-118">Specifies a daily, weekly, monthly, or a monthly day-of-the-week (DOW) trigger.</span></span><br/>   |
| [<span data-ttu-id="bbcd0-119">**EventTrigger**</span><span class="sxs-lookup"><span data-stu-id="bbcd0-119">**EventTrigger**</span></span>](taskschedulerschema-eventtrigger-triggergroup-element.md)               | [<span data-ttu-id="bbcd0-120">**eventTriggerType**</span><span class="sxs-lookup"><span data-stu-id="bbcd0-120">**eventTriggerType**</span></span>](taskschedulerschema-eventtriggertype-complextype.md)               | <span data-ttu-id="bbcd0-121">指定在發生系統事件時啟動工作的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="bbcd0-121">Specifies a trigger that starts a task when a system event occurs.</span></span><br/>                |
| [<span data-ttu-id="bbcd0-122">**IdleTrigger**</span><span class="sxs-lookup"><span data-stu-id="bbcd0-122">**IdleTrigger**</span></span>](taskschedulerschema-idletrigger-triggergroup-element.md)                 | [<span data-ttu-id="bbcd0-123">**idleTriggerType**</span><span class="sxs-lookup"><span data-stu-id="bbcd0-123">**idleTriggerType**</span></span>](taskschedulerschema-idletriggertype-complextype.md)                 | <span data-ttu-id="bbcd0-124">指定當電腦進入閒置狀態時啟動工作的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="bbcd0-124">Specifies a trigger that starts a task when the computer goes into an idle state.</span></span><br/> |
| [<span data-ttu-id="bbcd0-125">**LogonTrigger**</span><span class="sxs-lookup"><span data-stu-id="bbcd0-125">**LogonTrigger**</span></span>](taskschedulerschema-logontrigger-triggergroup-element.md)               | [<span data-ttu-id="bbcd0-126">**logonTriggerType**</span><span class="sxs-lookup"><span data-stu-id="bbcd0-126">**logonTriggerType**</span></span>](taskschedulerschema-logontriggertype-complextype.md)               | <span data-ttu-id="bbcd0-127">指定當使用者登入時啟動工作的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="bbcd0-127">Specifies a trigger that starts a task when a user logs on.</span></span><br/>                       |
| [<span data-ttu-id="bbcd0-128">**RegistrationTrigger**</span><span class="sxs-lookup"><span data-stu-id="bbcd0-128">**RegistrationTrigger**</span></span>](taskschedulerschema-registrationtrigger-triggergroup-element.md) | [<span data-ttu-id="bbcd0-129">**registrationTriggerType**</span><span class="sxs-lookup"><span data-stu-id="bbcd0-129">**registrationTriggerType**</span></span>](taskschedulerschema-registrationtriggertype-complextype.md) | <span data-ttu-id="bbcd0-130">指定在註冊工作時啟動工作的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="bbcd0-130">Specifies a trigger that starts a task when the task is registered.</span></span><br/>               |
| [<span data-ttu-id="bbcd0-131">**TimeTrigger**</span><span class="sxs-lookup"><span data-stu-id="bbcd0-131">**TimeTrigger**</span></span>](taskschedulerschema-timetrigger-triggergroup-element.md)                 | [<span data-ttu-id="bbcd0-132">**timeTriggerType**</span><span class="sxs-lookup"><span data-stu-id="bbcd0-132">**timeTriggerType**</span></span>](taskschedulerschema-timetriggertype-complextype.md)                 | <span data-ttu-id="bbcd0-133">指定啟動觸發程式時啟動工作的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="bbcd0-133">Specifies a trigger that starts a task when the trigger is activated.</span></span><br/>             |



## <a name="remarks"></a><span data-ttu-id="bbcd0-134">備註</span><span class="sxs-lookup"><span data-stu-id="bbcd0-134">Remarks</span></span>

<span data-ttu-id="bbcd0-135">針對開發腳本，會使用所有觸發程式物件所繼承的 [**Trigger.ExecutionTimeLimit**](trigger-executiontimelimit.md) 屬性來指定執行時間限制。</span><span class="sxs-lookup"><span data-stu-id="bbcd0-135">For scripting development, the execution time limit is specified using the [**Trigger.ExecutionTimeLimit**](trigger-executiontimelimit.md) property that is inherited by the all trigger objects.</span></span>

<span data-ttu-id="bbcd0-136">若是 c + + 開發，則會使用所有觸發程式介面所繼承的 [**ITrigger：： ExecutionTimeLimit**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_executiontimelimit) 屬性來指定執行時間限制。</span><span class="sxs-lookup"><span data-stu-id="bbcd0-136">For C++ development, the execution time limit is specified using the [**ITrigger::ExecutionTimeLimit**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_executiontimelimit) property that is inherited by the all trigger interfaces.</span></span>

## <a name="requirements"></a><span data-ttu-id="bbcd0-137">規格需求</span><span class="sxs-lookup"><span data-stu-id="bbcd0-137">Requirements</span></span>



| <span data-ttu-id="bbcd0-138">需求</span><span class="sxs-lookup"><span data-stu-id="bbcd0-138">Requirement</span></span> | <span data-ttu-id="bbcd0-139">值</span><span class="sxs-lookup"><span data-stu-id="bbcd0-139">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="bbcd0-140">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bbcd0-140">Minimum supported client</span></span><br/> | <span data-ttu-id="bbcd0-141">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bbcd0-141">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="bbcd0-142">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bbcd0-142">Minimum supported server</span></span><br/> | <span data-ttu-id="bbcd0-143">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bbcd0-143">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bbcd0-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bbcd0-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bbcd0-145">工作排程器架構元素</span><span class="sxs-lookup"><span data-stu-id="bbcd0-145">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="bbcd0-146">工作排程器</span><span class="sxs-lookup"><span data-stu-id="bbcd0-146">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





