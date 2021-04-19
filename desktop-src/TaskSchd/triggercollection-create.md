---
title: TriggerCollection. Create 方法
description: 針對腳本，會為工作建立新的觸發程式。
ms.assetid: 3d7dc811-0d83-475f-8a6e-87e59dae0113
keywords:
- 觸發程式工作排程器，建立
- 建立方法工作排程器
- 建立方法工作排程器，TriggerCollection 物件
- TriggerCollection 物件工作排程器，建立方法
topic_type:
- apiref
api_name:
- TriggerCollection.Create
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad0f1c5dd8bef3d81a8e9b5859bc2bbd8c969bf3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968952"
---
# <a name="triggercollectioncreate-method"></a><span data-ttu-id="14d65-107">TriggerCollection. Create 方法</span><span class="sxs-lookup"><span data-stu-id="14d65-107">TriggerCollection.Create method</span></span>

<span data-ttu-id="14d65-108">針對腳本，會為工作建立新的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="14d65-108">For scripting, creates a new trigger for the task.</span></span>

## <a name="syntax"></a><span data-ttu-id="14d65-109">語法</span><span class="sxs-lookup"><span data-stu-id="14d65-109">Syntax</span></span>


```VB
TriggerCollection.Create( _
  ByVal type _
)
```



## <a name="parameters"></a><span data-ttu-id="14d65-110">參數</span><span class="sxs-lookup"><span data-stu-id="14d65-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14d65-111">*類型* \[在\]</span><span class="sxs-lookup"><span data-stu-id="14d65-111">*type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14d65-112">此參數會設定為下列其中一個工作 [**\_ 觸發程式 \_ TYPE2**](/windows/desktop/api/taskschd/ne-taskschd-task_trigger_type2) 列舉常數。</span><span class="sxs-lookup"><span data-stu-id="14d65-112">This parameter is set to one of the following [**TASK\_TRIGGER\_TYPE2**](/windows/desktop/api/taskschd/ne-taskschd-task_trigger_type2) enumeration constants.</span></span>



| <span data-ttu-id="14d65-113">值</span><span class="sxs-lookup"><span data-stu-id="14d65-113">Value</span></span>                                                                                                                                                                                                                                                                                | <span data-ttu-id="14d65-114">意義</span><span class="sxs-lookup"><span data-stu-id="14d65-114">Meaning</span></span>                                                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_TRIGGER_EVENT"></span><span id="task_trigger_event"></span><dl> <span data-ttu-id="14d65-115"><dt>**工作 \_觸發程式 \_ 事件**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="14d65-115"><dt>**TASK\_TRIGGER\_EVENT**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="14d65-116">在特定事件發生時觸發工作。</span><span class="sxs-lookup"><span data-stu-id="14d65-116">Triggers the task when a specific event occurs.</span></span><br/>                                                                                                               |
| <span id="TASK_TRIGGER_TIME"></span><span id="task_trigger_time"></span><dl> <span data-ttu-id="14d65-117"><dt>**工作 \_觸發 \_ 時間**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="14d65-117"><dt>**TASK\_TRIGGER\_TIME**</dt> <dt>1</dt></span></span> </dl>                                                    | <span data-ttu-id="14d65-118">在一天中的特定時間觸發工作。</span><span class="sxs-lookup"><span data-stu-id="14d65-118">Triggers the task at a specific time of day.</span></span><br/>                                                                                                                  |
| <span id="TASK_TRIGGER_DAILY"></span><span id="task_trigger_daily"></span><dl> <span data-ttu-id="14d65-119"><dt>**工作 \_\_每日觸發**</dt>程式 <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="14d65-119"><dt>**TASK\_TRIGGER\_DAILY**</dt> <dt>2</dt></span></span> </dl>                                                 | <span data-ttu-id="14d65-120">依每日排程觸發工作。</span><span class="sxs-lookup"><span data-stu-id="14d65-120">Triggers the task on a daily schedule.</span></span> <span data-ttu-id="14d65-121">例如，工作會在每天、每隔三天、每隔三天的特定時間開始，依此類推。</span><span class="sxs-lookup"><span data-stu-id="14d65-121">For example, the task starts at a specific time every day, every-other day, every third day, and so on.</span></span><br/>                |
| <span id="TASK_TRIGGER_WEEKLY"></span><span id="task_trigger_weekly"></span><dl> <span data-ttu-id="14d65-122"><dt>**工作 \_\_每週**</dt> <dt>3</dt>個觸發程式</span><span class="sxs-lookup"><span data-stu-id="14d65-122"><dt>**TASK\_TRIGGER\_WEEKLY**</dt> <dt>3</dt></span></span> </dl>                                              | <span data-ttu-id="14d65-123">以每週排程觸發工作。</span><span class="sxs-lookup"><span data-stu-id="14d65-123">Triggers the task on a weekly schedule.</span></span> <span data-ttu-id="14d65-124">例如，工作會在每週或其他周的特定一天從上午8:00 開始。</span><span class="sxs-lookup"><span data-stu-id="14d65-124">For example, the task starts at 8:00 AM on a specific day every week or other week.</span></span><br/>                                   |
| <span id="TASK_TRIGGER_MONTHLY"></span><span id="task_trigger_monthly"></span><dl> <span data-ttu-id="14d65-125"><dt>**工作 \_\_每月**</dt> <dt>4 個</dt>觸發程式</span><span class="sxs-lookup"><span data-stu-id="14d65-125"><dt>**TASK\_TRIGGER\_MONTHLY**</dt> <dt>4</dt></span></span> </dl>                                           | <span data-ttu-id="14d65-126">依每月排程觸發工作。</span><span class="sxs-lookup"><span data-stu-id="14d65-126">Triggers the task on a monthly schedule.</span></span> <span data-ttu-id="14d65-127">例如，工作會在特定月份的特定日子開始。</span><span class="sxs-lookup"><span data-stu-id="14d65-127">For example, the task starts on specific days of specific months.</span></span><br/>                                                    |
| <span id="TASK_TRIGGER_MONTHLYDOW"></span><span id="task_trigger_monthlydow"></span><dl> <span data-ttu-id="14d65-128"><dt>**工作 \_觸發程式 \_ MONTHLYDOW**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="14d65-128"><dt>**TASK\_TRIGGER\_MONTHLYDOW**</dt> <dt>5</dt></span></span> </dl>                                  | <span data-ttu-id="14d65-129">會在每月的每週工作日排程上觸發工作。</span><span class="sxs-lookup"><span data-stu-id="14d65-129">Triggers the task on a monthly day-of-week schedule.</span></span> <span data-ttu-id="14d65-130">例如，工作會在一周的特定日子、每月的周數，以及當年的月份開始。</span><span class="sxs-lookup"><span data-stu-id="14d65-130">For example, the task starts on a specific days of the week, weeks of the month, and months of the year.</span></span><br/> |
| <span id="TASK_TRIGGER_IDLE"></span><span id="task_trigger_idle"></span><dl> <span data-ttu-id="14d65-131"><dt>**工作 \_觸發程式 \_ 閒置**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="14d65-131"><dt>**TASK\_TRIGGER\_IDLE**</dt> <dt>6</dt></span></span> </dl>                                                    | <span data-ttu-id="14d65-132">當電腦進入閒置狀態時，就會觸發工作。</span><span class="sxs-lookup"><span data-stu-id="14d65-132">Triggers the task when the computer goes into an idle state.</span></span><br/>                                                                                                  |
| <span id="TASK_TRIGGER_REGISTRATION"></span><span id="task_trigger_registration"></span><dl> <span data-ttu-id="14d65-133"><dt>**工作 \_觸發程式 \_ 註冊**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="14d65-133"><dt>**TASK\_TRIGGER\_REGISTRATION**</dt> <dt>7</dt></span></span> </dl>                            | <span data-ttu-id="14d65-134">在註冊工作時觸發工作。</span><span class="sxs-lookup"><span data-stu-id="14d65-134">Triggers the task when the task is registered.</span></span><br/>                                                                                                                |
| <span id="TASK_TRIGGER_BOOT"></span><span id="task_trigger_boot"></span><dl> <span data-ttu-id="14d65-135"><dt>**工作 \_觸發 \_ 開機**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="14d65-135"><dt>**TASK\_TRIGGER\_BOOT**</dt> <dt>8</dt></span></span> </dl>                                                    | <span data-ttu-id="14d65-136">在電腦開機時觸發工作。</span><span class="sxs-lookup"><span data-stu-id="14d65-136">Triggers the task when the computer boots.</span></span><br/>                                                                                                                    |
| <span id="TASK_TRIGGER_LOGON"></span><span id="task_trigger_logon"></span><dl> <span data-ttu-id="14d65-137"><dt>**工作 \_觸發程式 \_ 登**</dt>入 <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="14d65-137"><dt>**TASK\_TRIGGER\_LOGON**</dt> <dt>9</dt></span></span> </dl>                                                 | <span data-ttu-id="14d65-138">當特定使用者登入時觸發工作。</span><span class="sxs-lookup"><span data-stu-id="14d65-138">Triggers the task when a specific user logs on.</span></span><br/>                                                                                                               |
| <span id="TASK_TRIGGER_SESSION_STATE_CHANGE"></span><span id="task_trigger_session_state_change"></span><dl> <span data-ttu-id="14d65-139"><dt>**工作 \_觸發程式 \_ 會話 \_ 狀態 \_ 變更**</dt> <dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="14d65-139"><dt>**TASK\_TRIGGER\_SESSION\_STATE\_CHANGE**</dt> <dt>11</dt></span></span> </dl> | <span data-ttu-id="14d65-140">在特定會話狀態變更時觸發工作。</span><span class="sxs-lookup"><span data-stu-id="14d65-140">Triggers the task when a specific session state changes.</span></span><br/>                                                                                                      |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14d65-141">傳回值</span><span class="sxs-lookup"><span data-stu-id="14d65-141">Return value</span></span>

<span data-ttu-id="14d65-142">代表新觸發程式的 [**觸發**](trigger.md) 程式物件。</span><span class="sxs-lookup"><span data-stu-id="14d65-142">A [**Trigger**](trigger.md) object that represents the new trigger.</span></span>

## <a name="remarks"></a><span data-ttu-id="14d65-143">備註</span><span class="sxs-lookup"><span data-stu-id="14d65-143">Remarks</span></span>

<span data-ttu-id="14d65-144">如需每個觸發程式類型的詳細資訊，請參閱 [觸發程式類型](trigger-types.md)。</span><span class="sxs-lookup"><span data-stu-id="14d65-144">For information about each trigger type see [Trigger Types](trigger-types.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="14d65-145">規格需求</span><span class="sxs-lookup"><span data-stu-id="14d65-145">Requirements</span></span>



| <span data-ttu-id="14d65-146">需求</span><span class="sxs-lookup"><span data-stu-id="14d65-146">Requirement</span></span> | <span data-ttu-id="14d65-147">值</span><span class="sxs-lookup"><span data-stu-id="14d65-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="14d65-148">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="14d65-148">Minimum supported client</span></span><br/> | <span data-ttu-id="14d65-149">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="14d65-149">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="14d65-150">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="14d65-150">Minimum supported server</span></span><br/> | <span data-ttu-id="14d65-151">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="14d65-151">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="14d65-152">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="14d65-152">Type library</span></span><br/>             | <dl> <span data-ttu-id="14d65-153"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="14d65-153"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="14d65-154">DLL</span><span class="sxs-lookup"><span data-stu-id="14d65-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="14d65-155"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="14d65-155"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14d65-156">另請參閱</span><span class="sxs-lookup"><span data-stu-id="14d65-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14d65-157">工作排程器</span><span class="sxs-lookup"><span data-stu-id="14d65-157">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="14d65-158">**觸發**</span><span class="sxs-lookup"><span data-stu-id="14d65-158">**Trigger**</span></span>](trigger.md)
</dt> </dl>

 

 





