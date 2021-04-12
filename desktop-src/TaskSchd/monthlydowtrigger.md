---
title: MonthlyDOWTrigger 物件
description: 代表觸發程式的腳本物件，此觸發程式會在每個月的每週工作日排程啟動工作。
ms.assetid: 18607189-295f-4f7d-bf72-f0ac8d5067cf
keywords:
- 每月 DOW 觸發程式工作排程器，物件
- MonthlyDOWTrigger 物件工作排程器
- MonthlyDOWTrigger 物件工作排程器，說明
topic_type:
- apiref
api_name:
- MonthlyDOWTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b7e43925c6ebe27933a39fe5e25f37ffe6cf72e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024886"
---
# <a name="monthlydowtrigger-object"></a><span data-ttu-id="b6ca9-106">MonthlyDOWTrigger 物件</span><span class="sxs-lookup"><span data-stu-id="b6ca9-106">MonthlyDOWTrigger object</span></span>

<span data-ttu-id="b6ca9-107">代表觸發程式的腳本物件，此觸發程式會在每個月的每週工作日排程啟動工作。</span><span class="sxs-lookup"><span data-stu-id="b6ca9-107">Scripting object that represents a trigger that starts a task on a monthly day-of-week schedule.</span></span> <span data-ttu-id="b6ca9-108">例如，工作會在每個第一個星期四開始，可能到10月。</span><span class="sxs-lookup"><span data-stu-id="b6ca9-108">For example, the task starts on every first Thursday, May through October.</span></span>

## <a name="members"></a><span data-ttu-id="b6ca9-109">成員</span><span class="sxs-lookup"><span data-stu-id="b6ca9-109">Members</span></span>

<span data-ttu-id="b6ca9-110">**MonthlyDOWTrigger** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="b6ca9-110">The **MonthlyDOWTrigger** object has these types of members:</span></span>

-   [<span data-ttu-id="b6ca9-111">屬性</span><span class="sxs-lookup"><span data-stu-id="b6ca9-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b6ca9-112">屬性</span><span class="sxs-lookup"><span data-stu-id="b6ca9-112">Properties</span></span>

<span data-ttu-id="b6ca9-113">**MonthlyDOWTrigger** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="b6ca9-113">The **MonthlyDOWTrigger** object has these properties.</span></span>



| <span data-ttu-id="b6ca9-114">屬性</span><span class="sxs-lookup"><span data-stu-id="b6ca9-114">Property</span></span>                                                                          | <span data-ttu-id="b6ca9-115">存取類型</span><span class="sxs-lookup"><span data-stu-id="b6ca9-115">Access type</span></span>           | <span data-ttu-id="b6ca9-116">Description</span><span class="sxs-lookup"><span data-stu-id="b6ca9-116">Description</span></span>                                                                                                                                                                                 |
|:----------------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b6ca9-117">**DaysOfWeek**</span><span class="sxs-lookup"><span data-stu-id="b6ca9-117">**DaysOfWeek**</span></span>](monthlydowtrigger-daysofweek.md)<br/>                     | <span data-ttu-id="b6ca9-118">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b6ca9-118">Read/write</span></span><br/> | <span data-ttu-id="b6ca9-119">取得或設定工作在一周中的哪幾天執行。</span><span class="sxs-lookup"><span data-stu-id="b6ca9-119">Gets or sets the days of the week during which the task runs.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="b6ca9-120">**啟用**</span><span class="sxs-lookup"><span data-stu-id="b6ca9-120">**Enabled**</span></span>](trigger-enabled.md)<br/>                                     | <span data-ttu-id="b6ca9-121">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b6ca9-121">Read/write</span></span><br/> | <span data-ttu-id="b6ca9-122">繼承自 [**觸發**](trigger.md) 程式物件。</span><span class="sxs-lookup"><span data-stu-id="b6ca9-122">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="b6ca9-123">取得或設定布林值，這個值會指出是否已啟用觸發程式。</span><span class="sxs-lookup"><span data-stu-id="b6ca9-123">Gets or sets a Boolean value that indicates whether the trigger is enabled.</span></span><br/>                                                |
| [<span data-ttu-id="b6ca9-124">EndBoundary</span><span class="sxs-lookup"><span data-stu-id="b6ca9-124">EndBoundary</span></span>](trigger-endboundary.md)<br/>                                 | <span data-ttu-id="b6ca9-125">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b6ca9-125">Read/write</span></span><br/> | <span data-ttu-id="b6ca9-126">繼承自 [**觸發**](trigger.md) 程式物件。</span><span class="sxs-lookup"><span data-stu-id="b6ca9-126">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="b6ca9-127">取得或設定停用觸發程式的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="b6ca9-127">Gets or sets the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="b6ca9-128">觸發程式在停用之後無法啟動工作。</span><span class="sxs-lookup"><span data-stu-id="b6ca9-128">The trigger cannot start the task after it is deactivated.</span></span><br/> |
| [<span data-ttu-id="b6ca9-129">**ExecutionTimeLimit**</span><span class="sxs-lookup"><span data-stu-id="b6ca9-129">**ExecutionTimeLimit**</span></span>](trigger-executiontimelimit.md)<br/>               | <span data-ttu-id="b6ca9-130">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b6ca9-130">Read/write</span></span><br/> | <span data-ttu-id="b6ca9-131">繼承自 [**觸發**](trigger.md) 程式物件。</span><span class="sxs-lookup"><span data-stu-id="b6ca9-131">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="b6ca9-132">取得或設定允許執行此觸發程式之工作的最大時間量。</span><span class="sxs-lookup"><span data-stu-id="b6ca9-132">Gets or sets the maximum amount of time that the task launched by this trigger is allowed to run.</span></span><br/>                          |
| [<span data-ttu-id="b6ca9-133">**Id**</span><span class="sxs-lookup"><span data-stu-id="b6ca9-133">**Id**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                              | <span data-ttu-id="b6ca9-134">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b6ca9-134">Read/write</span></span><br/> | <span data-ttu-id="b6ca9-135">繼承自 [**觸發**](trigger.md) 程式物件。</span><span class="sxs-lookup"><span data-stu-id="b6ca9-135">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="b6ca9-136">取得或設定觸發程式的識別碼。</span><span class="sxs-lookup"><span data-stu-id="b6ca9-136">Gets or sets the identifier for the trigger.</span></span><br/>                                                                               |
| [<span data-ttu-id="b6ca9-137">**MonthsOfYear**</span><span class="sxs-lookup"><span data-stu-id="b6ca9-137">**MonthsOfYear**</span></span>](monthlydowtrigger-monthsofyear.md)<br/>                 | <span data-ttu-id="b6ca9-138">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b6ca9-138">Read/write</span></span><br/> | <span data-ttu-id="b6ca9-139">取得或設定工作在一年中執行的月份。</span><span class="sxs-lookup"><span data-stu-id="b6ca9-139">Gets or sets the months of the year during which the task runs.</span></span><br/>                                                                                                                  |
| [<span data-ttu-id="b6ca9-140">**RandomDelay**</span><span class="sxs-lookup"><span data-stu-id="b6ca9-140">**RandomDelay**</span></span>](monthlydowtrigger-randomdelay.md)<br/>                   | <span data-ttu-id="b6ca9-141">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b6ca9-141">Read/write</span></span><br/> | <span data-ttu-id="b6ca9-142">取得或設定隨機加入至觸發程式開始時間的延遲時間。</span><span class="sxs-lookup"><span data-stu-id="b6ca9-142">Gets or sets a delay time that is randomly added to the start time of the trigger.</span></span><br/>                                                                                               |
| [<span data-ttu-id="b6ca9-143">**重複**</span><span class="sxs-lookup"><span data-stu-id="b6ca9-143">**Repetition**</span></span>](trigger-repetition.md)<br/>                               | <span data-ttu-id="b6ca9-144">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b6ca9-144">Read/write</span></span><br/> | <span data-ttu-id="b6ca9-145">繼承自 [**觸發**](trigger.md) 程式物件。</span><span class="sxs-lookup"><span data-stu-id="b6ca9-145">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="b6ca9-146">取得或設定工作的執行頻率，以及啟動工作之後重複模式重複的時間長度。</span><span class="sxs-lookup"><span data-stu-id="b6ca9-146">Gets or sets how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/>          |
| [<span data-ttu-id="b6ca9-147">**RunOnLastWeekOfMonth**</span><span class="sxs-lookup"><span data-stu-id="b6ca9-147">**RunOnLastWeekOfMonth**</span></span>](monthlydowtrigger-runonlastweekofmonth.md)<br/> | <span data-ttu-id="b6ca9-148">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b6ca9-148">Read/write</span></span><br/> | <span data-ttu-id="b6ca9-149">取得或設定布林值，指出工作會在當月的最後一周執行。</span><span class="sxs-lookup"><span data-stu-id="b6ca9-149">Gets or sets a Boolean value that indicates that the task runs on the last week of the month.</span></span><br/>                                                                                    |
| [<span data-ttu-id="b6ca9-150">**StartBoundary**</span><span class="sxs-lookup"><span data-stu-id="b6ca9-150">**StartBoundary**</span></span>](trigger-startboundary.md)<br/>                         | <span data-ttu-id="b6ca9-151">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b6ca9-151">Read/write</span></span><br/> | <span data-ttu-id="b6ca9-152">繼承自 [**觸發**](trigger.md) 程式物件。</span><span class="sxs-lookup"><span data-stu-id="b6ca9-152">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="b6ca9-153">取得或設定啟動觸發程式的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="b6ca9-153">Gets or sets the date and time when the trigger is activated.</span></span><br/>                                                              |
| [<span data-ttu-id="b6ca9-154">**類型**</span><span class="sxs-lookup"><span data-stu-id="b6ca9-154">**Type**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                                          | <span data-ttu-id="b6ca9-155">唯讀</span><span class="sxs-lookup"><span data-stu-id="b6ca9-155">Read-only</span></span><br/>  | <span data-ttu-id="b6ca9-156">繼承自 [**觸發**](trigger.md) 程式物件。</span><span class="sxs-lookup"><span data-stu-id="b6ca9-156">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="b6ca9-157">取得觸發程式的類型。</span><span class="sxs-lookup"><span data-stu-id="b6ca9-157">Gets the type of the trigger.</span></span><br/>                                                                                              |
| [<span data-ttu-id="b6ca9-158">**WeeksOfMonth**</span><span class="sxs-lookup"><span data-stu-id="b6ca9-158">**WeeksOfMonth**</span></span>](monthlydowtrigger-weeksofmonth.md)<br/>                 | <span data-ttu-id="b6ca9-159">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b6ca9-159">Read/write</span></span><br/> | <span data-ttu-id="b6ca9-160">取得或設定工作執行的月份周數。</span><span class="sxs-lookup"><span data-stu-id="b6ca9-160">Gets or sets the weeks of the month during which the task runs.</span></span><br/>                                                                                                                  |



 

## <a name="remarks"></a><span data-ttu-id="b6ca9-161">備註</span><span class="sxs-lookup"><span data-stu-id="b6ca9-161">Remarks</span></span>

<span data-ttu-id="b6ca9-162">工作開始的當日時間是由 [**StartBoundary**](trigger-startboundary.md) 屬性所設定。</span><span class="sxs-lookup"><span data-stu-id="b6ca9-162">The time of day that the task is started is set by the [**StartBoundary**](trigger-startboundary.md) property.</span></span>

<span data-ttu-id="b6ca9-163">在讀取或寫入工作的 XML 時，會使用工作排程器架構的 [**ScheduleByMonthDayOfWeek**](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) 元素來指定每週的星期幾觸發程式。</span><span class="sxs-lookup"><span data-stu-id="b6ca9-163">When reading or writing XML for a task, a monthly day-of-week trigger is specified using the [**ScheduleByMonthDayOfWeek**](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6ca9-164">規格需求</span><span class="sxs-lookup"><span data-stu-id="b6ca9-164">Requirements</span></span>



| <span data-ttu-id="b6ca9-165">需求</span><span class="sxs-lookup"><span data-stu-id="b6ca9-165">Requirement</span></span> | <span data-ttu-id="b6ca9-166">值</span><span class="sxs-lookup"><span data-stu-id="b6ca9-166">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b6ca9-167">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b6ca9-167">Minimum supported client</span></span><br/> | <span data-ttu-id="b6ca9-168">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b6ca9-168">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="b6ca9-169">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b6ca9-169">Minimum supported server</span></span><br/> | <span data-ttu-id="b6ca9-170">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b6ca9-170">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b6ca9-171">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="b6ca9-171">Type library</span></span><br/>             | <dl> <span data-ttu-id="b6ca9-172"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b6ca9-172"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b6ca9-173">DLL</span><span class="sxs-lookup"><span data-stu-id="b6ca9-173">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b6ca9-174"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b6ca9-174"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6ca9-175">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b6ca9-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6ca9-176">**觸發**</span><span class="sxs-lookup"><span data-stu-id="b6ca9-176">**Trigger**</span></span>](trigger.md)
</dt> <dt>

[<span data-ttu-id="b6ca9-177">工作排程器物件</span><span class="sxs-lookup"><span data-stu-id="b6ca9-177">Task Scheduler Objects</span></span>](task-scheduler-objects.md)
</dt> <dt>

[<span data-ttu-id="b6ca9-178">工作排程器</span><span class="sxs-lookup"><span data-stu-id="b6ca9-178">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="b6ca9-179">**TriggerCollection**</span><span class="sxs-lookup"><span data-stu-id="b6ca9-179">**TriggerCollection**</span></span>](triggercollection.md)
</dt> <dt>

[<span data-ttu-id="b6ca9-180">**TriggerCollection 建立**</span><span class="sxs-lookup"><span data-stu-id="b6ca9-180">**TriggerCollection.Create**</span></span>](triggercollection-create.md)
</dt> </dl>

 

 





