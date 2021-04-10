---
title: MonthlyTrigger 物件
description: 腳本物件，代表根據每月排程啟動工作的觸發程式。
ms.assetid: d73715cb-a52e-4daf-930f-e94fbe28881e
keywords:
- 每月觸發程式工作排程器，物件
- MonthlyTrigger 物件工作排程器
- MonthlyTrigger 物件工作排程器，說明
topic_type:
- apiref
api_name:
- MonthlyTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce433f626fbe45e209f881c00787495cc6343bc1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686003"
---
# <a name="monthlytrigger-object"></a><span data-ttu-id="fdecd-106">MonthlyTrigger 物件</span><span class="sxs-lookup"><span data-stu-id="fdecd-106">MonthlyTrigger object</span></span>

<span data-ttu-id="fdecd-107">腳本物件，代表根據每月排程啟動工作的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="fdecd-107">Scripting object that represents a trigger that starts a task based on a monthly schedule.</span></span> <span data-ttu-id="fdecd-108">例如，工作會在特定月份的特定日子開始。</span><span class="sxs-lookup"><span data-stu-id="fdecd-108">For example, the task starts on specific days of specific months.</span></span>

## <a name="members"></a><span data-ttu-id="fdecd-109">成員</span><span class="sxs-lookup"><span data-stu-id="fdecd-109">Members</span></span>

<span data-ttu-id="fdecd-110">**MonthlyTrigger** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="fdecd-110">The **MonthlyTrigger** object has these types of members:</span></span>

-   [<span data-ttu-id="fdecd-111">屬性</span><span class="sxs-lookup"><span data-stu-id="fdecd-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fdecd-112">屬性</span><span class="sxs-lookup"><span data-stu-id="fdecd-112">Properties</span></span>

<span data-ttu-id="fdecd-113">**MonthlyTrigger** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="fdecd-113">The **MonthlyTrigger** object has these properties.</span></span>



| <span data-ttu-id="fdecd-114">屬性</span><span class="sxs-lookup"><span data-stu-id="fdecd-114">Property</span></span>                                                                     | <span data-ttu-id="fdecd-115">存取類型</span><span class="sxs-lookup"><span data-stu-id="fdecd-115">Access type</span></span>           | <span data-ttu-id="fdecd-116">Description</span><span class="sxs-lookup"><span data-stu-id="fdecd-116">Description</span></span>                                                                                                                                                                                 |
|:-----------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fdecd-117">**DaysOfMonth**</span><span class="sxs-lookup"><span data-stu-id="fdecd-117">**DaysOfMonth**</span></span>](monthlytrigger-daysofmonth.md)<br/>                 | <span data-ttu-id="fdecd-118">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="fdecd-118">Read/write</span></span><br/> | <span data-ttu-id="fdecd-119">取得或設定工作執行的當月天數。</span><span class="sxs-lookup"><span data-stu-id="fdecd-119">Gets or sets the days of the month during which the task runs.</span></span><br/>                                                                                                                   |
| [<span data-ttu-id="fdecd-120">**啟用**</span><span class="sxs-lookup"><span data-stu-id="fdecd-120">**Enabled**</span></span>](trigger-enabled.md)<br/>                                | <span data-ttu-id="fdecd-121">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="fdecd-121">Read/write</span></span><br/> | <span data-ttu-id="fdecd-122">繼承自 [**觸發**](trigger.md) 程式物件。</span><span class="sxs-lookup"><span data-stu-id="fdecd-122">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="fdecd-123">取得或設定布林值，這個值會指出是否已啟用觸發程式。</span><span class="sxs-lookup"><span data-stu-id="fdecd-123">Gets or sets a Boolean value that indicates whether the trigger is enabled.</span></span><br/>                                                |
| [<span data-ttu-id="fdecd-124">EndBoundary</span><span class="sxs-lookup"><span data-stu-id="fdecd-124">EndBoundary</span></span>](trigger-endboundary.md)<br/>                            | <span data-ttu-id="fdecd-125">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="fdecd-125">Read/write</span></span><br/> | <span data-ttu-id="fdecd-126">繼承自 [**觸發**](trigger.md) 程式物件。</span><span class="sxs-lookup"><span data-stu-id="fdecd-126">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="fdecd-127">取得或設定停用觸發程式的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="fdecd-127">Gets or sets the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="fdecd-128">觸發程式在停用之後無法啟動工作。</span><span class="sxs-lookup"><span data-stu-id="fdecd-128">The trigger cannot start the task after it is deactivated.</span></span><br/> |
| [<span data-ttu-id="fdecd-129">**ExecutionTimeLimit**</span><span class="sxs-lookup"><span data-stu-id="fdecd-129">**ExecutionTimeLimit**</span></span>](trigger-executiontimelimit.md)<br/>          | <span data-ttu-id="fdecd-130">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="fdecd-130">Read/write</span></span><br/> | <span data-ttu-id="fdecd-131">繼承自 [**觸發**](trigger.md) 程式物件。</span><span class="sxs-lookup"><span data-stu-id="fdecd-131">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="fdecd-132">取得或設定允許執行觸發程式之工作的最大時間量。</span><span class="sxs-lookup"><span data-stu-id="fdecd-132">Gets or sets the maximum amount of time that the task launched by the trigger is allowed to run.</span></span><br/>                           |
| [<span data-ttu-id="fdecd-133">**Id**</span><span class="sxs-lookup"><span data-stu-id="fdecd-133">**Id**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                         | <span data-ttu-id="fdecd-134">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="fdecd-134">Read/write</span></span><br/> | <span data-ttu-id="fdecd-135">繼承自 [**觸發**](trigger.md) 程式物件。</span><span class="sxs-lookup"><span data-stu-id="fdecd-135">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="fdecd-136">取得或設定觸發程式的識別碼。</span><span class="sxs-lookup"><span data-stu-id="fdecd-136">Gets or sets the identifier for the trigger.</span></span><br/>                                                                               |
| [<span data-ttu-id="fdecd-137">**MonthsOfYear**</span><span class="sxs-lookup"><span data-stu-id="fdecd-137">**MonthsOfYear**</span></span>](monthlytrigger-monthsofyear.md)<br/>               | <span data-ttu-id="fdecd-138">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="fdecd-138">Read/write</span></span><br/> | <span data-ttu-id="fdecd-139">取得或設定工作在一年中執行的月份。</span><span class="sxs-lookup"><span data-stu-id="fdecd-139">Gets or sets the months of the year during which the task runs.</span></span><br/>                                                                                                                  |
| [<span data-ttu-id="fdecd-140">**RandomDelay**</span><span class="sxs-lookup"><span data-stu-id="fdecd-140">**RandomDelay**</span></span>](monthlytrigger-randomdelay.md)<br/>                 | <span data-ttu-id="fdecd-141">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="fdecd-141">Read/write</span></span><br/> | <span data-ttu-id="fdecd-142">取得或設定隨機加入至觸發程式開始時間的延遲時間。</span><span class="sxs-lookup"><span data-stu-id="fdecd-142">Gets or sets a delay time that is randomly added to the start time of the trigger.</span></span><br/>                                                                                               |
| [<span data-ttu-id="fdecd-143">**重複**</span><span class="sxs-lookup"><span data-stu-id="fdecd-143">**Repetition**</span></span>](trigger-repetition.md)<br/>                          | <span data-ttu-id="fdecd-144">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="fdecd-144">Read/write</span></span><br/> | <span data-ttu-id="fdecd-145">繼承自 [**觸發**](trigger.md) 程式物件。</span><span class="sxs-lookup"><span data-stu-id="fdecd-145">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="fdecd-146">取得或設定工作的執行頻率，以及啟動工作之後重複模式重複的時間長度。</span><span class="sxs-lookup"><span data-stu-id="fdecd-146">Gets or sets how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/>          |
| [<span data-ttu-id="fdecd-147">**RunOnLastDayOfMonth**</span><span class="sxs-lookup"><span data-stu-id="fdecd-147">**RunOnLastDayOfMonth**</span></span>](monthlytrigger-runonlastdayofmonth.md)<br/> | <span data-ttu-id="fdecd-148">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="fdecd-148">Read/write</span></span><br/> | <span data-ttu-id="fdecd-149">取得或設定布林值，指出工作會在當月的最後一天執行。</span><span class="sxs-lookup"><span data-stu-id="fdecd-149">Gets or sets a Boolean value that indicates that the task runs on the last day of the month.</span></span><br/>                                                                                     |
| [<span data-ttu-id="fdecd-150">**StartBoundary**</span><span class="sxs-lookup"><span data-stu-id="fdecd-150">**StartBoundary**</span></span>](trigger-startboundary.md)<br/>                    | <span data-ttu-id="fdecd-151">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="fdecd-151">Read/write</span></span><br/> | <span data-ttu-id="fdecd-152">繼承自 [**觸發**](trigger.md) 程式物件。</span><span class="sxs-lookup"><span data-stu-id="fdecd-152">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="fdecd-153">取得或設定啟動觸發程式的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="fdecd-153">Gets or sets the date and time when the trigger is activated.</span></span><br/>                                                              |
| [<span data-ttu-id="fdecd-154">**類型**</span><span class="sxs-lookup"><span data-stu-id="fdecd-154">**Type**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                                     | <span data-ttu-id="fdecd-155">唯讀</span><span class="sxs-lookup"><span data-stu-id="fdecd-155">Read-only</span></span><br/>  | <span data-ttu-id="fdecd-156">繼承自 [**觸發**](trigger.md) 程式物件。</span><span class="sxs-lookup"><span data-stu-id="fdecd-156">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="fdecd-157">取得觸發程式的類型。</span><span class="sxs-lookup"><span data-stu-id="fdecd-157">Gets the type of the trigger.</span></span><br/>                                                                                              |



 

## <a name="remarks"></a><span data-ttu-id="fdecd-158">備註</span><span class="sxs-lookup"><span data-stu-id="fdecd-158">Remarks</span></span>

<span data-ttu-id="fdecd-159">工作開始的當日時間是由 [**StartBoundary**](trigger-startboundary.md) 屬性所設定。</span><span class="sxs-lookup"><span data-stu-id="fdecd-159">The time of day that the task is started is set by the [**StartBoundary**](trigger-startboundary.md) property.</span></span>

<span data-ttu-id="fdecd-160">針對工作讀取或撰寫您自己的 XML 時，會使用工作排程器架構的 [**ScheduleByMonth**](taskschedulerschema-schedulebymonth-calendartriggertype-element.md) 元素來指定每月觸發程式。</span><span class="sxs-lookup"><span data-stu-id="fdecd-160">When reading or writing your own XML for a task, a monthly trigger is specified using the [**ScheduleByMonth**](taskschedulerschema-schedulebymonth-calendartriggertype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="fdecd-161">規格需求</span><span class="sxs-lookup"><span data-stu-id="fdecd-161">Requirements</span></span>



| <span data-ttu-id="fdecd-162">需求</span><span class="sxs-lookup"><span data-stu-id="fdecd-162">Requirement</span></span> | <span data-ttu-id="fdecd-163">值</span><span class="sxs-lookup"><span data-stu-id="fdecd-163">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fdecd-164">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fdecd-164">Minimum supported client</span></span><br/> | <span data-ttu-id="fdecd-165">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fdecd-165">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="fdecd-166">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fdecd-166">Minimum supported server</span></span><br/> | <span data-ttu-id="fdecd-167">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fdecd-167">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="fdecd-168">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="fdecd-168">Type library</span></span><br/>             | <dl> <span data-ttu-id="fdecd-169"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="fdecd-169"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="fdecd-170">DLL</span><span class="sxs-lookup"><span data-stu-id="fdecd-170">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fdecd-171"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fdecd-171"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fdecd-172">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fdecd-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fdecd-173">**觸發**</span><span class="sxs-lookup"><span data-stu-id="fdecd-173">**Trigger**</span></span>](trigger.md)
</dt> <dt>

[<span data-ttu-id="fdecd-174">工作排程器物件</span><span class="sxs-lookup"><span data-stu-id="fdecd-174">Task Scheduler Objects</span></span>](task-scheduler-objects.md)
</dt> <dt>

[<span data-ttu-id="fdecd-175">工作排程器</span><span class="sxs-lookup"><span data-stu-id="fdecd-175">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="fdecd-176">**TriggerCollection**</span><span class="sxs-lookup"><span data-stu-id="fdecd-176">**TriggerCollection**</span></span>](triggercollection.md)
</dt> <dt>

[<span data-ttu-id="fdecd-177">**TriggerCollection 建立**</span><span class="sxs-lookup"><span data-stu-id="fdecd-177">**TriggerCollection.Create**</span></span>](triggercollection-create.md)
</dt> </dl>

 

 





