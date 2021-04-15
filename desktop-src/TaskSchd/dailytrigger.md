---
title: DailyTrigger 物件
description: 腳本物件，代表根據每日排程啟動工作的觸發程式。
ms.assetid: f03f53a0-0060-4793-96c1-b47a96852579
keywords:
- 每日觸發程式工作排程器，物件
- DailyTrigger 物件工作排程器
- DailyTrigger 物件工作排程器，說明
topic_type:
- apiref
api_name:
- DailyTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22203ecf7a421f07ccb823745e6619e05f84f550
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464817"
---
# <a name="dailytrigger-object"></a><span data-ttu-id="d4569-106">DailyTrigger 物件</span><span class="sxs-lookup"><span data-stu-id="d4569-106">DailyTrigger object</span></span>

<span data-ttu-id="d4569-107">腳本物件，代表根據每日排程啟動工作的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="d4569-107">Scripting object that represents a trigger that starts a task based on a daily schedule.</span></span>

## <a name="members"></a><span data-ttu-id="d4569-108">成員</span><span class="sxs-lookup"><span data-stu-id="d4569-108">Members</span></span>

<span data-ttu-id="d4569-109">**DailyTrigger** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="d4569-109">The **DailyTrigger** object has these types of members:</span></span>

-   [<span data-ttu-id="d4569-110">屬性</span><span class="sxs-lookup"><span data-stu-id="d4569-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d4569-111">屬性</span><span class="sxs-lookup"><span data-stu-id="d4569-111">Properties</span></span>

<span data-ttu-id="d4569-112">**DailyTrigger** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="d4569-112">The **DailyTrigger** object has these properties.</span></span>



| <span data-ttu-id="d4569-113">屬性</span><span class="sxs-lookup"><span data-stu-id="d4569-113">Property</span></span>                                                            | <span data-ttu-id="d4569-114">存取類型</span><span class="sxs-lookup"><span data-stu-id="d4569-114">Access type</span></span>           | <span data-ttu-id="d4569-115">Description</span><span class="sxs-lookup"><span data-stu-id="d4569-115">Description</span></span>                                                                                                                                                                                 |
|:--------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d4569-116">**DaysInterval**</span><span class="sxs-lookup"><span data-stu-id="d4569-116">**DaysInterval**</span></span>](dailytrigger-daysinterval.md)<br/>        | <span data-ttu-id="d4569-117">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="d4569-117">Read/write</span></span><br/> | <span data-ttu-id="d4569-118">取得或設定排程中天數之間的間隔。</span><span class="sxs-lookup"><span data-stu-id="d4569-118">Gets or sets the interval between the days in the schedule.</span></span><br/>                                                                                                                      |
| [<span data-ttu-id="d4569-119">**啟用**</span><span class="sxs-lookup"><span data-stu-id="d4569-119">**Enabled**</span></span>](trigger-enabled.md)<br/>                       | <span data-ttu-id="d4569-120">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="d4569-120">Read/write</span></span><br/> | <span data-ttu-id="d4569-121">繼承自 [**觸發**](trigger.md) 程式物件。</span><span class="sxs-lookup"><span data-stu-id="d4569-121">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="d4569-122">取得或設定布林值，這個值會指出是否已啟用觸發程式。</span><span class="sxs-lookup"><span data-stu-id="d4569-122">Gets or sets a Boolean value that indicates whether the trigger is enabled.</span></span><br/>                                                |
| [<span data-ttu-id="d4569-123">**EndBoundary**</span><span class="sxs-lookup"><span data-stu-id="d4569-123">**EndBoundary**</span></span>](trigger-endboundary.md)<br/>               | <span data-ttu-id="d4569-124">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="d4569-124">Read/write</span></span><br/> | <span data-ttu-id="d4569-125">繼承自 [**觸發**](trigger.md) 程式物件。</span><span class="sxs-lookup"><span data-stu-id="d4569-125">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="d4569-126">取得或設定停用觸發程式的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="d4569-126">Gets or sets the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="d4569-127">觸發程式在停用之後無法啟動工作。</span><span class="sxs-lookup"><span data-stu-id="d4569-127">The trigger cannot start the task after it is deactivated.</span></span><br/> |
| [<span data-ttu-id="d4569-128">**ExecutionTimeLimit**</span><span class="sxs-lookup"><span data-stu-id="d4569-128">**ExecutionTimeLimit**</span></span>](trigger-executiontimelimit.md)<br/> | <span data-ttu-id="d4569-129">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="d4569-129">Read/write</span></span><br/> | <span data-ttu-id="d4569-130">繼承自 [**觸發**](trigger.md) 程式物件。</span><span class="sxs-lookup"><span data-stu-id="d4569-130">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="d4569-131">取得或設定允許執行觸發程式之工作的最大時間量。</span><span class="sxs-lookup"><span data-stu-id="d4569-131">Gets or sets the maximum amount of time that the task launched by the trigger is allowed to run.</span></span><br/>                           |
| [<span data-ttu-id="d4569-132">**Id**</span><span class="sxs-lookup"><span data-stu-id="d4569-132">**Id**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                | <span data-ttu-id="d4569-133">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="d4569-133">Read/write</span></span><br/> | <span data-ttu-id="d4569-134">繼承自 [**觸發**](trigger.md) 程式物件。</span><span class="sxs-lookup"><span data-stu-id="d4569-134">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="d4569-135">取得或設定觸發程式的識別碼。</span><span class="sxs-lookup"><span data-stu-id="d4569-135">Gets or sets the identifier for the trigger.</span></span><br/>                                                                               |
| [<span data-ttu-id="d4569-136">**RandomDelay**</span><span class="sxs-lookup"><span data-stu-id="d4569-136">**RandomDelay**</span></span>](dailytrigger-randomdelay.md)<br/>          | <span data-ttu-id="d4569-137">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="d4569-137">Read/write</span></span><br/> | <span data-ttu-id="d4569-138">取得或設定隨機加入至觸發程式開始時間的延遲時間。</span><span class="sxs-lookup"><span data-stu-id="d4569-138">Gets or sets a delay time that is randomly added to the start time of the trigger.</span></span><br/>                                                                                               |
| [<span data-ttu-id="d4569-139">**重複**</span><span class="sxs-lookup"><span data-stu-id="d4569-139">**Repetition**</span></span>](trigger-repetition.md)<br/>                 | <span data-ttu-id="d4569-140">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="d4569-140">Read/write</span></span><br/> | <span data-ttu-id="d4569-141">繼承自 [**觸發**](trigger.md) 程式物件。</span><span class="sxs-lookup"><span data-stu-id="d4569-141">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="d4569-142">取得或設定工作的執行頻率，以及啟動工作之後重複模式重複的時間長度。</span><span class="sxs-lookup"><span data-stu-id="d4569-142">Gets or sets how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/>          |
| [<span data-ttu-id="d4569-143">**StartBoundary**</span><span class="sxs-lookup"><span data-stu-id="d4569-143">**StartBoundary**</span></span>](trigger-startboundary.md)<br/>           | <span data-ttu-id="d4569-144">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="d4569-144">Read/write</span></span><br/> | <span data-ttu-id="d4569-145">繼承自 [**觸發**](trigger.md) 程式物件。</span><span class="sxs-lookup"><span data-stu-id="d4569-145">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="d4569-146">取得或設定啟動觸發程式的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="d4569-146">Gets or sets the date and time when the trigger is activated.</span></span><br/>                                                              |
| [<span data-ttu-id="d4569-147">**類型**</span><span class="sxs-lookup"><span data-stu-id="d4569-147">**Type**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                            | <span data-ttu-id="d4569-148">唯讀</span><span class="sxs-lookup"><span data-stu-id="d4569-148">Read-only</span></span><br/>  | <span data-ttu-id="d4569-149">繼承自 [**觸發**](trigger.md) 程式物件。</span><span class="sxs-lookup"><span data-stu-id="d4569-149">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="d4569-150">取得觸發程式的類型。</span><span class="sxs-lookup"><span data-stu-id="d4569-150">Gets the type of the trigger.</span></span><br/>                                                                                              |



 

## <a name="remarks"></a><span data-ttu-id="d4569-151">備註</span><span class="sxs-lookup"><span data-stu-id="d4569-151">Remarks</span></span>

<span data-ttu-id="d4569-152">工作開始的當日時間是由 [**StartBoundary**](trigger-startboundary.md) 屬性所設定。</span><span class="sxs-lookup"><span data-stu-id="d4569-152">The time of day that the task is started is set by the [**StartBoundary**](trigger-startboundary.md) property.</span></span>

<span data-ttu-id="d4569-153">間隔1會產生每日排程。</span><span class="sxs-lookup"><span data-stu-id="d4569-153">An interval of 1 produces a daily schedule.</span></span> <span data-ttu-id="d4569-154">間隔2會產生每隔一天的排程，依此類推。</span><span class="sxs-lookup"><span data-stu-id="d4569-154">An interval of 2 produces an every other day schedule and so on.</span></span>

<span data-ttu-id="d4569-155">針對工作讀取或撰寫您自己的 XML 時，會使用工作排程器架構的 [**ScheduleByDay**](taskschedulerschema-schedulebyday-calendartriggertype-element.md) 元素來指定每日觸發程式。</span><span class="sxs-lookup"><span data-stu-id="d4569-155">When reading or writing your own XML for a task, a daily trigger is specified using the [**ScheduleByDay**](taskschedulerschema-schedulebyday-calendartriggertype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="examples"></a><span data-ttu-id="d4569-156">範例</span><span class="sxs-lookup"><span data-stu-id="d4569-156">Examples</span></span>

<span data-ttu-id="d4569-157">如需此腳本物件的詳細資訊和程式碼範例，請參閱 [ (腳本) 的每日觸發程式範例 ](daily-trigger-example--scripting-.md)。</span><span class="sxs-lookup"><span data-stu-id="d4569-157">For more information and a code example for this scripting object, see [Daily Trigger Example (Scripting)](daily-trigger-example--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d4569-158">規格需求</span><span class="sxs-lookup"><span data-stu-id="d4569-158">Requirements</span></span>



| <span data-ttu-id="d4569-159">需求</span><span class="sxs-lookup"><span data-stu-id="d4569-159">Requirement</span></span> | <span data-ttu-id="d4569-160">值</span><span class="sxs-lookup"><span data-stu-id="d4569-160">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d4569-161">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d4569-161">Minimum supported client</span></span><br/> | <span data-ttu-id="d4569-162">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d4569-162">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="d4569-163">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d4569-163">Minimum supported server</span></span><br/> | <span data-ttu-id="d4569-164">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d4569-164">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d4569-165">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="d4569-165">Type library</span></span><br/>             | <dl> <span data-ttu-id="d4569-166"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d4569-166"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d4569-167">DLL</span><span class="sxs-lookup"><span data-stu-id="d4569-167">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d4569-168"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d4569-168"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4569-169">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d4569-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4569-170">**觸發**</span><span class="sxs-lookup"><span data-stu-id="d4569-170">**Trigger**</span></span>](trigger.md)
</dt> <dt>

[<span data-ttu-id="d4569-171">**TriggerCollection**</span><span class="sxs-lookup"><span data-stu-id="d4569-171">**TriggerCollection**</span></span>](triggercollection.md)
</dt> <dt>

[<span data-ttu-id="d4569-172">**TriggerCollection 建立**</span><span class="sxs-lookup"><span data-stu-id="d4569-172">**TriggerCollection.Create**</span></span>](triggercollection-create.md)
</dt> </dl>

 

 





