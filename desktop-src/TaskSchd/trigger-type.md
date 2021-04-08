---
title: Trigger。 Type 屬性
description: 針對腳本，會取得觸發程式的類型。
ms.assetid: 346e6b02-c89e-4644-aa19-2bbf3d0fb3c3
keywords:
- Type 屬性工作排程器
- 類型屬性工作排程器，觸發程式物件
- 觸發程式物件工作排程器，類型屬性
topic_type:
- apiref
api_name:
- Trigger.Type
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba2cef2d6ae33ceeac028e10a0f545afbc0a0ec8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685730"
---
# <a name="triggertype-property"></a><span data-ttu-id="4affc-106">Trigger。 Type 屬性</span><span class="sxs-lookup"><span data-stu-id="4affc-106">Trigger.Type property</span></span>

<span data-ttu-id="4affc-107">針對腳本，會取得觸發程式的類型。</span><span class="sxs-lookup"><span data-stu-id="4affc-107">For scripting, gets the type of the trigger.</span></span> <span data-ttu-id="4affc-108">觸發程式類型是在建立觸發程式時定義的，而且稍後無法變更。</span><span class="sxs-lookup"><span data-stu-id="4affc-108">The trigger type is defined when the trigger is created and cannot be changed later.</span></span> <span data-ttu-id="4affc-109">如需建立觸發程式的詳細資訊，請參閱 [**TriggerCollection。**](triggercollection-create.md)</span><span class="sxs-lookup"><span data-stu-id="4affc-109">For information on creating a trigger, see [**TriggerCollection.Create**](triggercollection-create.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="4affc-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="4affc-110">Syntax</span></span>


```VB
Trigger.Type As TASK_TRIGGER_TYPE2
```



## <a name="property-value"></a><span data-ttu-id="4affc-111">屬性值</span><span class="sxs-lookup"><span data-stu-id="4affc-111">Property value</span></span>

<span data-ttu-id="4affc-112">下列其中一個工作 [**\_ 觸發程式 \_ TYPE2**](/windows/desktop/api/taskschd/ne-taskschd-task_trigger_type2) 列舉值。</span><span class="sxs-lookup"><span data-stu-id="4affc-112">One of the following [**TASK\_TRIGGER\_TYPE2**](/windows/desktop/api/taskschd/ne-taskschd-task_trigger_type2) enumeration values.</span></span>



| <span data-ttu-id="4affc-113">值</span><span class="sxs-lookup"><span data-stu-id="4affc-113">Value</span></span>                                                                                                                                                                                                                                                                                | <span data-ttu-id="4affc-114">意義</span><span class="sxs-lookup"><span data-stu-id="4affc-114">Meaning</span></span>                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <span id="TASK_TRIGGER_EVENT"></span><span id="task_trigger_event"></span><dl> <span data-ttu-id="4affc-115"><dt>**工作 \_觸發程式 \_ 事件**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="4affc-115"><dt>**TASK\_TRIGGER\_EVENT**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="4affc-116">在特定事件發生時啟動工作。</span><span class="sxs-lookup"><span data-stu-id="4affc-116">Starts the task when a specific event occurs.</span></span><br/>              |
| <span id="TASK_TRIGGER_TIME"></span><span id="task_trigger_time"></span><dl> <span data-ttu-id="4affc-117"><dt>**工作 \_觸發 \_ 時間**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="4affc-117"><dt>**TASK\_TRIGGER\_TIME**</dt> <dt>1</dt></span></span> </dl>                                                    | <span data-ttu-id="4affc-118">在一天中的特定時間啟動工作。</span><span class="sxs-lookup"><span data-stu-id="4affc-118">Starts the task at a specific time of day.</span></span><br/>                 |
| <span id="TASK_TRIGGER_DAILY"></span><span id="task_trigger_daily"></span><dl> <span data-ttu-id="4affc-119"><dt>**工作 \_\_每日觸發**</dt>程式 <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="4affc-119"><dt>**TASK\_TRIGGER\_DAILY**</dt> <dt>2</dt></span></span> </dl>                                                 | <span data-ttu-id="4affc-120">每天啟動工作。</span><span class="sxs-lookup"><span data-stu-id="4affc-120">Starts the task daily.</span></span><br/>                                     |
| <span id="TASK_TRIGGER_WEEKLY"></span><span id="task_trigger_weekly"></span><dl> <span data-ttu-id="4affc-121"><dt>**工作 \_\_每週**</dt> <dt>3</dt>個觸發程式</span><span class="sxs-lookup"><span data-stu-id="4affc-121"><dt>**TASK\_TRIGGER\_WEEKLY**</dt> <dt>3</dt></span></span> </dl>                                              | <span data-ttu-id="4affc-122">每週啟動工作。</span><span class="sxs-lookup"><span data-stu-id="4affc-122">Starts the task weekly.</span></span><br/>                                    |
| <span id="TASK_TRIGGER_MONTHLY"></span><span id="task_trigger_monthly"></span><dl> <span data-ttu-id="4affc-123"><dt>**工作 \_\_每月**</dt> <dt>4 個</dt>觸發程式</span><span class="sxs-lookup"><span data-stu-id="4affc-123"><dt>**TASK\_TRIGGER\_MONTHLY**</dt> <dt>4</dt></span></span> </dl>                                           | <span data-ttu-id="4affc-124">每月啟動工作。</span><span class="sxs-lookup"><span data-stu-id="4affc-124">Starts the task monthly.</span></span><br/>                                   |
| <span id="TASK_TRIGGER_MONTHLYDOW"></span><span id="task_trigger_monthlydow"></span><dl> <span data-ttu-id="4affc-125"><dt>**工作 \_觸發程式 \_ MONTHLYDOW**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="4affc-125"><dt>**TASK\_TRIGGER\_MONTHLYDOW**</dt> <dt>5</dt></span></span> </dl>                                  | <span data-ttu-id="4affc-126">在每個月于一周的特定一天啟動工作。</span><span class="sxs-lookup"><span data-stu-id="4affc-126">Starts the task every month on a specific day of the week.</span></span><br/> |
| <span id="TASK_TRIGGER_IDLE"></span><span id="task_trigger_idle"></span><dl> <span data-ttu-id="4affc-127"><dt>**工作 \_觸發程式 \_ 閒置**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="4affc-127"><dt>**TASK\_TRIGGER\_IDLE**</dt> <dt>6</dt></span></span> </dl>                                                    | <span data-ttu-id="4affc-128">當電腦進入閒置狀態時，就會啟動工作。</span><span class="sxs-lookup"><span data-stu-id="4affc-128">Starts the task when the computer goes into an idle state.</span></span><br/> |
| <span id="TASK_TRIGGER_REGISTRATION"></span><span id="task_trigger_registration"></span><dl> <span data-ttu-id="4affc-129"><dt>**工作 \_觸發程式 \_ 註冊**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="4affc-129"><dt>**TASK\_TRIGGER\_REGISTRATION**</dt> <dt>7</dt></span></span> </dl>                            | <span data-ttu-id="4affc-130">在註冊工作時啟動工作。</span><span class="sxs-lookup"><span data-stu-id="4affc-130">Starts the task when the task is registered.</span></span><br/>               |
| <span id="TASK_TRIGGER_BOOT"></span><span id="task_trigger_boot"></span><dl> <span data-ttu-id="4affc-131"><dt>**工作 \_觸發 \_ 開機**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="4affc-131"><dt>**TASK\_TRIGGER\_BOOT**</dt> <dt>8</dt></span></span> </dl>                                                    | <span data-ttu-id="4affc-132">當電腦啟動時啟動工作。</span><span class="sxs-lookup"><span data-stu-id="4affc-132">Starts the task when the computer boots.</span></span><br/>                   |
| <span id="TASK_TRIGGER_LOGON"></span><span id="task_trigger_logon"></span><dl> <span data-ttu-id="4affc-133"><dt>**工作 \_觸發程式 \_ 登**</dt>入 <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="4affc-133"><dt>**TASK\_TRIGGER\_LOGON**</dt> <dt>9</dt></span></span> </dl>                                                 | <span data-ttu-id="4affc-134">在特定使用者登入時啟動工作。</span><span class="sxs-lookup"><span data-stu-id="4affc-134">Starts the task when a specific user logs on.</span></span><br/>              |
| <span id="TASK_TRIGGER_SESSION_STATE_CHANGE"></span><span id="task_trigger_session_state_change"></span><dl> <span data-ttu-id="4affc-135"><dt>**工作 \_觸發程式 \_ 會話 \_ 狀態 \_ 變更**</dt> <dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="4affc-135"><dt>**TASK\_TRIGGER\_SESSION\_STATE\_CHANGE**</dt> <dt>11</dt></span></span> </dl> | <span data-ttu-id="4affc-136">在特定會話狀態變更時觸發工作。</span><span class="sxs-lookup"><span data-stu-id="4affc-136">Triggers the task when a specific session state changes.</span></span><br/>   |



 

## <a name="requirements"></a><span data-ttu-id="4affc-137">規格需求</span><span class="sxs-lookup"><span data-stu-id="4affc-137">Requirements</span></span>



| <span data-ttu-id="4affc-138">需求</span><span class="sxs-lookup"><span data-stu-id="4affc-138">Requirement</span></span> | <span data-ttu-id="4affc-139">值</span><span class="sxs-lookup"><span data-stu-id="4affc-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4affc-140">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4affc-140">Minimum supported client</span></span><br/> | <span data-ttu-id="4affc-141">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4affc-141">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="4affc-142">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4affc-142">Minimum supported server</span></span><br/> | <span data-ttu-id="4affc-143">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4affc-143">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4affc-144">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="4affc-144">Type library</span></span><br/>             | <dl> <span data-ttu-id="4affc-145"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="4affc-145"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="4affc-146">DLL</span><span class="sxs-lookup"><span data-stu-id="4affc-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4affc-147"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4affc-147"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4affc-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4affc-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4affc-149">**TriggerCollection 建立**</span><span class="sxs-lookup"><span data-stu-id="4affc-149">**TriggerCollection.Create**</span></span>](triggercollection-create.md)
</dt> <dt>

[<span data-ttu-id="4affc-150">**工作 \_ 觸發程式 \_ TYPE2**</span><span class="sxs-lookup"><span data-stu-id="4affc-150">**TASK\_TRIGGER\_TYPE2**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_trigger_type2)
</dt> <dt>

[<span data-ttu-id="4affc-151">工作排程器</span><span class="sxs-lookup"><span data-stu-id="4affc-151">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





