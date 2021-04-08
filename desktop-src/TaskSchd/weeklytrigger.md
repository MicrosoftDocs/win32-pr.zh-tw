---
title: WeeklyTrigger 物件
description: 腳本物件，代表根據每週排程啟動工作的觸發程式。
ms.assetid: a000d7a8-0239-440f-b49b-7f0c55b01e8e
keywords:
- 每週觸發程式工作排程器，物件
- WeeklyTrigger 物件工作排程器
- WeeklyTrigger 物件工作排程器，說明
topic_type:
- apiref
api_name:
- WeeklyTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58dec9172d38b53f779f44a048b39bc709dbd54f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686603"
---
# <a name="weeklytrigger-object"></a><span data-ttu-id="5b7f6-106">WeeklyTrigger 物件</span><span class="sxs-lookup"><span data-stu-id="5b7f6-106">WeeklyTrigger object</span></span>

<span data-ttu-id="5b7f6-107">腳本物件，代表根據每週排程啟動工作的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="5b7f6-107">Scripting object that represents a trigger that starts a task based on a weekly schedule.</span></span> <span data-ttu-id="5b7f6-108">例如，工作從上午8:00 開始。</span><span class="sxs-lookup"><span data-stu-id="5b7f6-108">For example, the task starts at 8:00 A.M.</span></span> <span data-ttu-id="5b7f6-109">在每週或每週的特定一天。</span><span class="sxs-lookup"><span data-stu-id="5b7f6-109">on a specific day of the week every week or every other week.</span></span>

## <a name="members"></a><span data-ttu-id="5b7f6-110">成員</span><span class="sxs-lookup"><span data-stu-id="5b7f6-110">Members</span></span>

<span data-ttu-id="5b7f6-111">**WeeklyTrigger** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="5b7f6-111">The **WeeklyTrigger** object has these types of members:</span></span>

-   [<span data-ttu-id="5b7f6-112">屬性</span><span class="sxs-lookup"><span data-stu-id="5b7f6-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5b7f6-113">屬性</span><span class="sxs-lookup"><span data-stu-id="5b7f6-113">Properties</span></span>

<span data-ttu-id="5b7f6-114">**WeeklyTrigger** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="5b7f6-114">The **WeeklyTrigger** object has these properties.</span></span>



| <span data-ttu-id="5b7f6-115">屬性</span><span class="sxs-lookup"><span data-stu-id="5b7f6-115">Property</span></span>                                                            | <span data-ttu-id="5b7f6-116">存取類型</span><span class="sxs-lookup"><span data-stu-id="5b7f6-116">Access type</span></span>           | <span data-ttu-id="5b7f6-117">Description</span><span class="sxs-lookup"><span data-stu-id="5b7f6-117">Description</span></span>                                                                                                                                                                                 |
|:--------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5b7f6-118">**DaysOfWeek**</span><span class="sxs-lookup"><span data-stu-id="5b7f6-118">**DaysOfWeek**</span></span>](weeklytrigger-daysofweek.md)<br/>           | <span data-ttu-id="5b7f6-119">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="5b7f6-119">Read/write</span></span><br/> | <span data-ttu-id="5b7f6-120">取得或設定工作在一周中的哪幾天執行。</span><span class="sxs-lookup"><span data-stu-id="5b7f6-120">Gets or sets the days of the week on which the task runs.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="5b7f6-121">**啟用**</span><span class="sxs-lookup"><span data-stu-id="5b7f6-121">**Enabled**</span></span>](trigger-enabled.md)<br/>                       | <span data-ttu-id="5b7f6-122">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="5b7f6-122">Read/write</span></span><br/> | <span data-ttu-id="5b7f6-123">繼承自 [**觸發**](trigger.md) 程式物件。</span><span class="sxs-lookup"><span data-stu-id="5b7f6-123">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="5b7f6-124">取得或設定布林值，這個值會指出是否已啟用觸發程式。</span><span class="sxs-lookup"><span data-stu-id="5b7f6-124">Gets or sets a Boolean value that indicates whether the trigger is enabled.</span></span><br/>                                                |
| [<span data-ttu-id="5b7f6-125">**EndBoundary**</span><span class="sxs-lookup"><span data-stu-id="5b7f6-125">**EndBoundary**</span></span>](trigger-endboundary.md)<br/>               | <span data-ttu-id="5b7f6-126">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="5b7f6-126">Read/write</span></span><br/> | <span data-ttu-id="5b7f6-127">繼承自 [**觸發**](trigger.md) 程式物件。</span><span class="sxs-lookup"><span data-stu-id="5b7f6-127">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="5b7f6-128">取得或設定停用觸發程式的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="5b7f6-128">Gets or sets the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="5b7f6-129">觸發程式在停用之後無法啟動工作。</span><span class="sxs-lookup"><span data-stu-id="5b7f6-129">The trigger cannot start the task after it is deactivated.</span></span><br/> |
| [<span data-ttu-id="5b7f6-130">**ExecutionTimeLimit**</span><span class="sxs-lookup"><span data-stu-id="5b7f6-130">**ExecutionTimeLimit**</span></span>](trigger-executiontimelimit.md)<br/> | <span data-ttu-id="5b7f6-131">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="5b7f6-131">Read/write</span></span><br/> | <span data-ttu-id="5b7f6-132">繼承自 [**觸發**](trigger.md) 程式物件。</span><span class="sxs-lookup"><span data-stu-id="5b7f6-132">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="5b7f6-133">取得或設定允許執行觸發程式之工作的最大時間量。</span><span class="sxs-lookup"><span data-stu-id="5b7f6-133">Gets or sets the maximum amount of time that the task launched by the trigger is allowed to run.</span></span><br/>                           |
| [<span data-ttu-id="5b7f6-134">**Id**</span><span class="sxs-lookup"><span data-stu-id="5b7f6-134">**Id**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                | <span data-ttu-id="5b7f6-135">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="5b7f6-135">Read/write</span></span><br/> | <span data-ttu-id="5b7f6-136">繼承自 [**觸發**](trigger.md) 程式物件。</span><span class="sxs-lookup"><span data-stu-id="5b7f6-136">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="5b7f6-137">取得或設定觸發程式的識別碼。</span><span class="sxs-lookup"><span data-stu-id="5b7f6-137">Gets or sets the identifier for the trigger.</span></span><br/>                                                                               |
| [<span data-ttu-id="5b7f6-138">**RandomDelay**</span><span class="sxs-lookup"><span data-stu-id="5b7f6-138">**RandomDelay**</span></span>](weeklytrigger-randomdelay.md)<br/>         | <span data-ttu-id="5b7f6-139">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="5b7f6-139">Read/write</span></span><br/> | <span data-ttu-id="5b7f6-140">取得或設定隨機加入至觸發程式開始時間的延遲時間。</span><span class="sxs-lookup"><span data-stu-id="5b7f6-140">Gets or sets a delay time that is randomly added to the start time of the trigger.</span></span><br/>                                                                                               |
| [<span data-ttu-id="5b7f6-141">**重複**</span><span class="sxs-lookup"><span data-stu-id="5b7f6-141">**Repetition**</span></span>](trigger-repetition.md)<br/>                 | <span data-ttu-id="5b7f6-142">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="5b7f6-142">Read/write</span></span><br/> | <span data-ttu-id="5b7f6-143">繼承自 [**觸發**](trigger.md) 程式物件。</span><span class="sxs-lookup"><span data-stu-id="5b7f6-143">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="5b7f6-144">取得或設定工作的執行頻率，以及啟動工作之後重複模式重複的時間長度。</span><span class="sxs-lookup"><span data-stu-id="5b7f6-144">Gets or sets how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/>          |
| [<span data-ttu-id="5b7f6-145">**StartBoundary**</span><span class="sxs-lookup"><span data-stu-id="5b7f6-145">**StartBoundary**</span></span>](trigger-startboundary.md)<br/>           | <span data-ttu-id="5b7f6-146">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="5b7f6-146">Read/write</span></span><br/> | <span data-ttu-id="5b7f6-147">繼承自 [**觸發**](trigger.md) 程式物件。</span><span class="sxs-lookup"><span data-stu-id="5b7f6-147">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="5b7f6-148">取得或設定啟動觸發程式的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="5b7f6-148">Gets or sets the date and time when the trigger is activated.</span></span><br/>                                                              |
| [<span data-ttu-id="5b7f6-149">**類型**</span><span class="sxs-lookup"><span data-stu-id="5b7f6-149">**Type**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                            | <span data-ttu-id="5b7f6-150">唯讀</span><span class="sxs-lookup"><span data-stu-id="5b7f6-150">Read-only</span></span><br/>  | <span data-ttu-id="5b7f6-151">繼承自 [**觸發**](trigger.md) 程式物件。</span><span class="sxs-lookup"><span data-stu-id="5b7f6-151">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="5b7f6-152">取得觸發程式的類型。</span><span class="sxs-lookup"><span data-stu-id="5b7f6-152">Gets the type of the trigger.</span></span><br/>                                                                                              |
| [<span data-ttu-id="5b7f6-153">**WeeksInterval**</span><span class="sxs-lookup"><span data-stu-id="5b7f6-153">**WeeksInterval**</span></span>](weeklytrigger-weeksinterval.md)<br/>     | <span data-ttu-id="5b7f6-154">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="5b7f6-154">Read/write</span></span><br/> | <span data-ttu-id="5b7f6-155">取得或設定排程中周之間的間隔。</span><span class="sxs-lookup"><span data-stu-id="5b7f6-155">Gets or sets the interval between the weeks in the schedule.</span></span><br/>                                                                                                                     |



 

## <a name="remarks"></a><span data-ttu-id="5b7f6-156">備註</span><span class="sxs-lookup"><span data-stu-id="5b7f6-156">Remarks</span></span>

<span data-ttu-id="5b7f6-157">工作開始的當日時間是由 [**StartBoundary**](trigger-startboundary.md) 屬性所設定。</span><span class="sxs-lookup"><span data-stu-id="5b7f6-157">The time of day that the task is started is set by the [**StartBoundary**](trigger-startboundary.md) property.</span></span>

<span data-ttu-id="5b7f6-158">針對工作讀取或撰寫您自己的 XML 時，會使用工作排程器架構的 [**ScheduleByWeek**](taskschedulerschema-schedulebyweek-calendartriggertype-element.md) 元素來指定每週觸發程式。</span><span class="sxs-lookup"><span data-stu-id="5b7f6-158">When reading or writing your own XML for a task, a weekly trigger is specified using the [**ScheduleByWeek**](taskschedulerschema-schedulebyweek-calendartriggertype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="examples"></a><span data-ttu-id="5b7f6-159">範例</span><span class="sxs-lookup"><span data-stu-id="5b7f6-159">Examples</span></span>

<span data-ttu-id="5b7f6-160">如需此腳本物件的詳細資訊和程式碼範例，請參閱 [ (腳本) 的每週觸發程式範例 ](weekly-trigger-example--scripting-.md)。</span><span class="sxs-lookup"><span data-stu-id="5b7f6-160">For more information and a code example for this scripting object, see [Weekly Trigger Example (Scripting)](weekly-trigger-example--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5b7f6-161">規格需求</span><span class="sxs-lookup"><span data-stu-id="5b7f6-161">Requirements</span></span>



| <span data-ttu-id="5b7f6-162">需求</span><span class="sxs-lookup"><span data-stu-id="5b7f6-162">Requirement</span></span> | <span data-ttu-id="5b7f6-163">值</span><span class="sxs-lookup"><span data-stu-id="5b7f6-163">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5b7f6-164">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5b7f6-164">Minimum supported client</span></span><br/> | <span data-ttu-id="5b7f6-165">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5b7f6-165">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="5b7f6-166">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5b7f6-166">Minimum supported server</span></span><br/> | <span data-ttu-id="5b7f6-167">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5b7f6-167">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5b7f6-168">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="5b7f6-168">Type library</span></span><br/>             | <dl> <span data-ttu-id="5b7f6-169"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="5b7f6-169"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="5b7f6-170">DLL</span><span class="sxs-lookup"><span data-stu-id="5b7f6-170">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5b7f6-171"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5b7f6-171"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b7f6-172">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5b7f6-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b7f6-173">**觸發**</span><span class="sxs-lookup"><span data-stu-id="5b7f6-173">**Trigger**</span></span>](trigger.md)
</dt> <dt>

[<span data-ttu-id="5b7f6-174">**TriggerCollection**</span><span class="sxs-lookup"><span data-stu-id="5b7f6-174">**TriggerCollection**</span></span>](triggercollection.md)
</dt> <dt>

[<span data-ttu-id="5b7f6-175">**TriggerCollection 建立**</span><span class="sxs-lookup"><span data-stu-id="5b7f6-175">**TriggerCollection.Create**</span></span>](triggercollection-create.md)
</dt> </dl>

 

 





