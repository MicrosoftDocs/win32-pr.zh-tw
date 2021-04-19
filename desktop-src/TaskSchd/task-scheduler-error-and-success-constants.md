---
title: '工作排程器錯誤和成功常數 (Winerror.h) '
description: 如果發生錯誤，工作排程器 Api 可能會傳回下列其中一個錯誤碼作為 HRESULT 值。
ms.assetid: 54278bbd-7dca-438e-a771-5fcb08c4aa68
keywords:
- 工作排程器工作排程器、參考、錯誤和成功常數
topic_type:
- apiref
api_name:
- SCHED_S_TASK_READY
- SCHED_S_TASK_RUNNING
- SCHED_S_TASK_DISABLED
- SCHED_S_TASK_HAS_NOT_RUN
- SCHED_S_TASK_NO_MORE_RUNS
- SCHED_S_TASK_NOT_SCHEDULED
- SCHED_S_TASK_TERMINATED
- SCHED_S_TASK_NO_VALID_TRIGGERS
- SCHED_S_EVENT_TRIGGER
- SCHED_E_TRIGGER_NOT_FOUND
- SCHED_E_TASK_NOT_READY
- SCHED_E_TASK_NOT_RUNNING
- SCHED_E_SERVICE_NOT_INSTALLED
- SCHED_E_CANNOT_OPEN_TASK
- SCHED_E_INVALID_TASK
- SCHED_E_ACCOUNT_INFORMATION_NOT_SET
- SCHED_E_ACCOUNT_NAME_NOT_FOUND
- SCHED_E_ACCOUNT_DBASE_CORRUPT
- SCHED_E_NO_SECURITY_SERVICES
- SCHED_E_UNKNOWN_OBJECT_VERSION
- SCHED_E_UNSUPPORTED_ACCOUNT_OPTION
- SCHED_E_SERVICE_NOT_RUNNING
- SCHED_E_UNEXPECTEDNODE
- SCHED_E_NAMESPACE
- SCHED_E_INVALIDVALUE
- SCHED_E_MISSINGNODE
- SCHED_E_MALFORMEDXML
- SCHED_S_SOME_TRIGGERS_FAILED
- SCHED_S_BATCH_LOGON_PROBLEM
- SCHED_E_TOO_MANY_NODES
- SCHED_E_PAST_END_BOUNDARY
- SCHED_E_ALREADY_RUNNING
- SCHED_E_USER_NOT_LOGGED_ON
- SCHED_E_INVALID_TASK_HASH
- SCHED_E_SERVICE_NOT_AVAILABLE
- SCHED_E_SERVICE_TOO_BUSY
- SCHED_E_TASK_ATTEMPTED
- SCHED_S_TASK_QUEUED
- SCHED_E_TASK_DISABLED
- SCHED_E_TASK_NOT_V1_COMPAT
- SCHED_E_START_ON_DEMAND
api_location:
- WinError.h
api_type:
- HeaderDef
ms.topic: reference
ms.custom: snippet-project
ms.date: 05/31/2018
ms.openlocfilehash: a1d0347938020ca8937f2764e3b2c62a38fc9273
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993967"
---
# <a name="task-scheduler-error-and-success-constants"></a><span data-ttu-id="6d3d3-104">工作排程器錯誤和成功常數</span><span class="sxs-lookup"><span data-stu-id="6d3d3-104">Task Scheduler Error and Success Constants</span></span>

<span data-ttu-id="6d3d3-105">如果發生錯誤，工作排程器 Api 可能會傳回下列其中一個錯誤碼作為 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="6d3d3-105">If an error occurs, the Task Scheduler APIs can return one of the following error codes as an **HRESULT** value.</span></span>

<span data-ttu-id="6d3d3-106">以已計畫的開頭的 \_ 常數 \_ 是成功常數，而以已計畫 E 開頭的 \_ 常數 \_ 則是錯誤常數。</span><span class="sxs-lookup"><span data-stu-id="6d3d3-106">The constants that begin with SCHED\_S\_ are success constants, and the constants that begin with SCHED\_E\_ are error constants.</span></span>

```cpp
  HRESULT phrStatus;
  hr = pITask->GetStatus(&phrStatus);
  
  // Release the ITask interface.
  pITask->Release();
    
  switch(phrStatus)
  {
  case SCHED_S_TASK_READY:
       wprintf(L"  SCHED_S_TASK_READY\n");
       break;
  case SCHED_S_TASK_RUNNING:
       wprintf(L"  SCHED_S_TASK_RUNNING\n");
       break;

  //...
  }
```

<span data-ttu-id="6d3d3-107">[C/c + + 程式碼範例：正在](c-c-code-example-retrieving-task-status.md)抓取工作狀態。</span><span class="sxs-lookup"><span data-stu-id="6d3d3-107">Example from [C/C++ Code Example: Retrieving Task Status](c-c-code-example-retrieving-task-status.md).</span></span>

> [!Note]  
> <span data-ttu-id="6d3d3-108">某些工作排程器 Api 可能會傳回 (64 的系統和網路錯誤碼，例如) 。</span><span class="sxs-lookup"><span data-stu-id="6d3d3-108">Some Task Scheduler APIs can return system and network error codes (64 for example).</span></span> <span data-ttu-id="6d3d3-109">您可以在 [命令提示字元] 視窗中，使用 **net helpmsg** 命令檢查這些類型之錯誤碼的定義。</span><span class="sxs-lookup"><span data-stu-id="6d3d3-109">You can check the definition of these types of error codes by using the **net helpmsg** command in the command prompt window.</span></span> <span data-ttu-id="6d3d3-110">例如， **net helpmsg 64** 命令會傳回訊息：指定的網路名稱已無法再使用。</span><span class="sxs-lookup"><span data-stu-id="6d3d3-110">For example, the command **net helpmsg 64** returns the message: The specified network name is no longer available.</span></span>

 

<span data-ttu-id="6d3d3-111">如需事件和錯誤訊息的詳細資訊，請參閱 [事件和錯誤訊息中心](https://www.microsoft.com/technet/support/ee/ee_advanced.aspx)。</span><span class="sxs-lookup"><span data-stu-id="6d3d3-111">For more information about events and error messages, see [Events and Errors Message Center](https://www.microsoft.com/technet/support/ee/ee_advanced.aspx).</span></span>

<dl> <dt>

<span data-ttu-id="6d3d3-112"><span id="SCHED_S_TASK_READY"></span><span id="sched_s_task_ready"></span>**已計畫的工作已 \_ \_ \_ 就緒**</span><span class="sxs-lookup"><span data-stu-id="6d3d3-112"><span id="SCHED_S_TASK_READY"></span><span id="sched_s_task_ready"></span>**SCHED\_S\_TASK\_READY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d3d3-113">0x00041300</span><span class="sxs-lookup"><span data-stu-id="6d3d3-113">0x00041300</span></span>
</dt> <dt>



<span data-ttu-id="6d3d3-114">工作已準備好在下次排程的時間執行。</span><span class="sxs-lookup"><span data-stu-id="6d3d3-114">The task is ready to run at its next scheduled time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6d3d3-115"><span id="SCHED_S_TASK_RUNNING"></span><span id="sched_s_task_running"></span>**已計畫的工作 \_ \_ \_ 正在執行**</span><span class="sxs-lookup"><span data-stu-id="6d3d3-115"><span id="SCHED_S_TASK_RUNNING"></span><span id="sched_s_task_running"></span>**SCHED\_S\_TASK\_RUNNING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d3d3-116">0x00041301</span><span class="sxs-lookup"><span data-stu-id="6d3d3-116">0x00041301</span></span>
</dt> <dt>



<span data-ttu-id="6d3d3-117">工作目前正在執行。</span><span class="sxs-lookup"><span data-stu-id="6d3d3-117">The task is currently running.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6d3d3-118"><span id="SCHED_S_TASK_DISABLED"></span><span id="sched_s_task_disabled"></span>**\_ \_ \_ 已停用已計畫的工作**</span><span class="sxs-lookup"><span data-stu-id="6d3d3-118"><span id="SCHED_S_TASK_DISABLED"></span><span id="sched_s_task_disabled"></span>**SCHED\_S\_TASK\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d3d3-119">0x00041302</span><span class="sxs-lookup"><span data-stu-id="6d3d3-119">0x00041302</span></span>
</dt> <dt>



<span data-ttu-id="6d3d3-120">工作將不會在排程的時間執行，因為它已停用。</span><span class="sxs-lookup"><span data-stu-id="6d3d3-120">The task will not run at the scheduled times because it has been disabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6d3d3-121"><span id="SCHED_S_TASK_HAS_NOT_RUN"></span><span id="sched_s_task_has_not_run"></span>**\_已計畫 \_ 的 \_ 工作 \_ 尚未 \_ 執行**</span><span class="sxs-lookup"><span data-stu-id="6d3d3-121"><span id="SCHED_S_TASK_HAS_NOT_RUN"></span><span id="sched_s_task_has_not_run"></span>**SCHED\_S\_TASK\_HAS\_NOT\_RUN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d3d3-122">0x00041303</span><span class="sxs-lookup"><span data-stu-id="6d3d3-122">0x00041303</span></span>
</dt> <dt>



<span data-ttu-id="6d3d3-123">尚未執行此工作。</span><span class="sxs-lookup"><span data-stu-id="6d3d3-123">The task has not yet run.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6d3d3-124"><span id="SCHED_S_TASK_NO_MORE_RUNS"></span><span id="sched_s_task_no_more_runs"></span>**已計畫的工作 \_ \_ 不會 \_ 再 \_ \_ 執行**</span><span class="sxs-lookup"><span data-stu-id="6d3d3-124"><span id="SCHED_S_TASK_NO_MORE_RUNS"></span><span id="sched_s_task_no_more_runs"></span>**SCHED\_S\_TASK\_NO\_MORE\_RUNS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d3d3-125">0x00041304</span><span class="sxs-lookup"><span data-stu-id="6d3d3-125">0x00041304</span></span>
</dt> <dt>



<span data-ttu-id="6d3d3-126">尚未針對此工作排程執行任何執行。</span><span class="sxs-lookup"><span data-stu-id="6d3d3-126">There are no more runs scheduled for this task.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6d3d3-127"><span id="SCHED_S_TASK_NOT_SCHEDULED"></span><span id="sched_s_task_not_scheduled"></span>**\_ \_ \_ 未排程的已 \_ 計畫工作**</span><span class="sxs-lookup"><span data-stu-id="6d3d3-127"><span id="SCHED_S_TASK_NOT_SCHEDULED"></span><span id="sched_s_task_not_scheduled"></span>**SCHED\_S\_TASK\_NOT\_SCHEDULED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d3d3-128">0x00041305</span><span class="sxs-lookup"><span data-stu-id="6d3d3-128">0x00041305</span></span>
</dt> <dt>



<span data-ttu-id="6d3d3-129">尚未設定在排程上執行此工作所需的一或多個屬性。</span><span class="sxs-lookup"><span data-stu-id="6d3d3-129">One or more of the properties that are needed to run this task on a schedule have not been set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6d3d3-130"><span id="SCHED_S_TASK_TERMINATED"></span><span id="sched_s_task_terminated"></span>**已計畫的工作 \_ \_ \_ 終止**</span><span class="sxs-lookup"><span data-stu-id="6d3d3-130"><span id="SCHED_S_TASK_TERMINATED"></span><span id="sched_s_task_terminated"></span>**SCHED\_S\_TASK\_TERMINATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d3d3-131">0x00041306</span><span class="sxs-lookup"><span data-stu-id="6d3d3-131">0x00041306</span></span>
</dt> <dt>



<span data-ttu-id="6d3d3-132">上次執行的工作是由使用者終止。</span><span class="sxs-lookup"><span data-stu-id="6d3d3-132">The last run of the task was terminated by the user.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6d3d3-133"><span id="SCHED_S_TASK_NO_VALID_TRIGGERS"></span><span id="sched_s_task_no_valid_triggers"></span>**已計畫的工作 \_ \_ \_ 沒有 \_ 有效的 \_ 觸發程式**</span><span class="sxs-lookup"><span data-stu-id="6d3d3-133"><span id="SCHED_S_TASK_NO_VALID_TRIGGERS"></span><span id="sched_s_task_no_valid_triggers"></span>**SCHED\_S\_TASK\_NO\_VALID\_TRIGGERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d3d3-134">0x00041307</span><span class="sxs-lookup"><span data-stu-id="6d3d3-134">0x00041307</span></span>
</dt> <dt>



<span data-ttu-id="6d3d3-135">這項工作沒有觸發程式，或現有的觸發程式已停用或未設定。</span><span class="sxs-lookup"><span data-stu-id="6d3d3-135">Either the task has no triggers or the existing triggers are disabled or not set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6d3d3-136"><span id="SCHED_S_EVENT_TRIGGER"></span><span id="sched_s_event_trigger"></span>**已計畫的 \_ S \_ 事件 \_ 觸發程式**</span><span class="sxs-lookup"><span data-stu-id="6d3d3-136"><span id="SCHED_S_EVENT_TRIGGER"></span><span id="sched_s_event_trigger"></span>**SCHED\_S\_EVENT\_TRIGGER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d3d3-137">0x00041308</span><span class="sxs-lookup"><span data-stu-id="6d3d3-137">0x00041308</span></span>
</dt> <dt>



<span data-ttu-id="6d3d3-138">事件觸發程式沒有設定執行時間。</span><span class="sxs-lookup"><span data-stu-id="6d3d3-138">Event triggers do not have set run times.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6d3d3-139"><span id="SCHED_E_TRIGGER_NOT_FOUND"></span><span id="sched_e_trigger_not_found"></span>**\_ \_ \_ \_ 找不到已計畫的電子觸發程式**</span><span class="sxs-lookup"><span data-stu-id="6d3d3-139"><span id="SCHED_E_TRIGGER_NOT_FOUND"></span><span id="sched_e_trigger_not_found"></span>**SCHED\_E\_TRIGGER\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d3d3-140">0x80041309</span><span class="sxs-lookup"><span data-stu-id="6d3d3-140">0x80041309</span></span>
</dt> <dt>



<span data-ttu-id="6d3d3-141">找不到工作的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="6d3d3-141">A task's trigger is not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6d3d3-142"><span id="SCHED_E_TASK_NOT_READY"></span><span id="sched_e_task_not_ready"></span>**已計畫的 \_ 電子工作 \_ \_ 未 \_ 就緒**</span><span class="sxs-lookup"><span data-stu-id="6d3d3-142"><span id="SCHED_E_TASK_NOT_READY"></span><span id="sched_e_task_not_ready"></span>**SCHED\_E\_TASK\_NOT\_READY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d3d3-143">0x8004130A</span><span class="sxs-lookup"><span data-stu-id="6d3d3-143">0x8004130A</span></span>
</dt> <dt>



<span data-ttu-id="6d3d3-144">尚未設定執行此工作所需的一或多個屬性。</span><span class="sxs-lookup"><span data-stu-id="6d3d3-144">One or more of the properties required to run this task have not been set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6d3d3-145"><span id="SCHED_E_TASK_NOT_RUNNING"></span><span id="sched_e_task_not_running"></span>**已計畫的 \_ 電子工作 \_ \_ 未 \_ 執行**</span><span class="sxs-lookup"><span data-stu-id="6d3d3-145"><span id="SCHED_E_TASK_NOT_RUNNING"></span><span id="sched_e_task_not_running"></span>**SCHED\_E\_TASK\_NOT\_RUNNING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d3d3-146">0x8004130B</span><span class="sxs-lookup"><span data-stu-id="6d3d3-146">0x8004130B</span></span>
</dt> <dt>



<span data-ttu-id="6d3d3-147">沒有任何正在執行的工作實例。</span><span class="sxs-lookup"><span data-stu-id="6d3d3-147">There is no running instance of the task.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6d3d3-148"><span id="SCHED_E_SERVICE_NOT_INSTALLED"></span><span id="sched_e_service_not_installed"></span>**\_ \_ \_ 未 \_ 安裝已計畫的電子服務**</span><span class="sxs-lookup"><span data-stu-id="6d3d3-148"><span id="SCHED_E_SERVICE_NOT_INSTALLED"></span><span id="sched_e_service_not_installed"></span>**SCHED\_E\_SERVICE\_NOT\_INSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d3d3-149">0x8004130C</span><span class="sxs-lookup"><span data-stu-id="6d3d3-149">0x8004130C</span></span>
</dt> <dt>



<span data-ttu-id="6d3d3-150">這部電腦上未安裝工作排程器服務。</span><span class="sxs-lookup"><span data-stu-id="6d3d3-150">The Task Scheduler service is not installed on this computer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6d3d3-151"><span id="SCHED_E_CANNOT_OPEN_TASK"></span><span id="sched_e_cannot_open_task"></span>**已計畫的 \_ 電子 \_ 無法 \_ 開啟 \_ 工作**</span><span class="sxs-lookup"><span data-stu-id="6d3d3-151"><span id="SCHED_E_CANNOT_OPEN_TASK"></span><span id="sched_e_cannot_open_task"></span>**SCHED\_E\_CANNOT\_OPEN\_TASK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d3d3-152">0x8004130D</span><span class="sxs-lookup"><span data-stu-id="6d3d3-152">0x8004130D</span></span>
</dt> <dt>



<span data-ttu-id="6d3d3-153">無法開啟工作物件。</span><span class="sxs-lookup"><span data-stu-id="6d3d3-153">The task object could not be opened.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6d3d3-154"><span id="SCHED_E_INVALID_TASK"></span><span id="sched_e_invalid_task"></span>**已計畫 \_ 電子 \_ 不正確 \_ 工作**</span><span class="sxs-lookup"><span data-stu-id="6d3d3-154"><span id="SCHED_E_INVALID_TASK"></span><span id="sched_e_invalid_task"></span>**SCHED\_E\_INVALID\_TASK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d3d3-155">0x8004130E</span><span class="sxs-lookup"><span data-stu-id="6d3d3-155">0x8004130E</span></span>
</dt> <dt>



<span data-ttu-id="6d3d3-156">物件可能是不正確工作物件，或不是工作物件。</span><span class="sxs-lookup"><span data-stu-id="6d3d3-156">The object is either an invalid task object or is not a task object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6d3d3-157"><span id="SCHED_E_ACCOUNT_INFORMATION_NOT_SET"></span><span id="sched_e_account_information_not_set"></span>**未設定已計畫的 \_ 電子 \_ 帳戶 \_ 資訊 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6d3d3-157"><span id="SCHED_E_ACCOUNT_INFORMATION_NOT_SET"></span><span id="sched_e_account_information_not_set"></span>**SCHED\_E\_ACCOUNT\_INFORMATION\_NOT\_SET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d3d3-158">0x8004130F</span><span class="sxs-lookup"><span data-stu-id="6d3d3-158">0x8004130F</span></span>
</dt> <dt>



<span data-ttu-id="6d3d3-159">在指定之工作的工作排程器安全性資料庫中，找不到任何帳戶資訊。</span><span class="sxs-lookup"><span data-stu-id="6d3d3-159">No account information could be found in the Task Scheduler security database for the task indicated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6d3d3-160"><span id="SCHED_E_ACCOUNT_NAME_NOT_FOUND"></span><span id="sched_e_account_name_not_found"></span>**\_ \_ \_ \_ \_ 找不到已計畫的電子帳戶名稱**</span><span class="sxs-lookup"><span data-stu-id="6d3d3-160"><span id="SCHED_E_ACCOUNT_NAME_NOT_FOUND"></span><span id="sched_e_account_name_not_found"></span>**SCHED\_E\_ACCOUNT\_NAME\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d3d3-161">0x80041310</span><span class="sxs-lookup"><span data-stu-id="6d3d3-161">0x80041310</span></span>
</dt> <dt>



<span data-ttu-id="6d3d3-162">無法建立指定的帳號存在。</span><span class="sxs-lookup"><span data-stu-id="6d3d3-162">Unable to establish existence of the account specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6d3d3-163"><span id="SCHED_E_ACCOUNT_DBASE_CORRUPT"></span><span id="sched_e_account_dbase_corrupt"></span>**已計畫的 \_ 電子 \_ 帳戶 \_ DBASE \_ 損毀**</span><span class="sxs-lookup"><span data-stu-id="6d3d3-163"><span id="SCHED_E_ACCOUNT_DBASE_CORRUPT"></span><span id="sched_e_account_dbase_corrupt"></span>**SCHED\_E\_ACCOUNT\_DBASE\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d3d3-164">0x80041311</span><span class="sxs-lookup"><span data-stu-id="6d3d3-164">0x80041311</span></span>
</dt> <dt>



<span data-ttu-id="6d3d3-165">在工作排程器安全性資料庫中偵測到損毀;資料庫已重設。</span><span class="sxs-lookup"><span data-stu-id="6d3d3-165">Corruption was detected in the Task Scheduler security database; the database has been reset.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6d3d3-166"><span id="SCHED_E_NO_SECURITY_SERVICES"></span><span id="sched_e_no_security_services"></span>**未計畫的 \_ 電子 \_ \_ 安全性 \_ 服務**</span><span class="sxs-lookup"><span data-stu-id="6d3d3-166"><span id="SCHED_E_NO_SECURITY_SERVICES"></span><span id="sched_e_no_security_services"></span>**SCHED\_E\_NO\_SECURITY\_SERVICES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d3d3-167">0x80041312</span><span class="sxs-lookup"><span data-stu-id="6d3d3-167">0x80041312</span></span>
</dt> <dt>



<span data-ttu-id="6d3d3-168">工作排程器的安全性服務僅適用于 Windows NT。</span><span class="sxs-lookup"><span data-stu-id="6d3d3-168">Task Scheduler security services are available only on Windows NT.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6d3d3-169"><span id="SCHED_E_UNKNOWN_OBJECT_VERSION"></span><span id="sched_e_unknown_object_version"></span>**已計畫 \_ 電子 \_ 未知 \_ 物件 \_ 版本**</span><span class="sxs-lookup"><span data-stu-id="6d3d3-169"><span id="SCHED_E_UNKNOWN_OBJECT_VERSION"></span><span id="sched_e_unknown_object_version"></span>**SCHED\_E\_UNKNOWN\_OBJECT\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d3d3-170">0x80041313</span><span class="sxs-lookup"><span data-stu-id="6d3d3-170">0x80041313</span></span>
</dt> <dt>



<span data-ttu-id="6d3d3-171">工作物件版本可能不受支援或無效。</span><span class="sxs-lookup"><span data-stu-id="6d3d3-171">The task object version is either unsupported or invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6d3d3-172"><span id="SCHED_E_UNSUPPORTED_ACCOUNT_OPTION"></span><span id="sched_e_unsupported_account_option"></span>**已計畫 \_ 電子 \_ 不支援的 \_ 帳戶 \_ 選項**</span><span class="sxs-lookup"><span data-stu-id="6d3d3-172"><span id="SCHED_E_UNSUPPORTED_ACCOUNT_OPTION"></span><span id="sched_e_unsupported_account_option"></span>**SCHED\_E\_UNSUPPORTED\_ACCOUNT\_OPTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d3d3-173">0x80041314</span><span class="sxs-lookup"><span data-stu-id="6d3d3-173">0x80041314</span></span>
</dt> <dt>



<span data-ttu-id="6d3d3-174">已使用不支援的帳戶設定和執行時間選項群組合來設定工作。</span><span class="sxs-lookup"><span data-stu-id="6d3d3-174">The task has been configured with an unsupported combination of account settings and run time options.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6d3d3-175"><span id="SCHED_E_SERVICE_NOT_RUNNING"></span><span id="sched_e_service_not_running"></span>**已計畫的 \_ E \_ 服務 \_ 未 \_ 執行**</span><span class="sxs-lookup"><span data-stu-id="6d3d3-175"><span id="SCHED_E_SERVICE_NOT_RUNNING"></span><span id="sched_e_service_not_running"></span>**SCHED\_E\_SERVICE\_NOT\_RUNNING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d3d3-176">0x80041315</span><span class="sxs-lookup"><span data-stu-id="6d3d3-176">0x80041315</span></span>
</dt> <dt>



<span data-ttu-id="6d3d3-177">工作排程器服務未執行。</span><span class="sxs-lookup"><span data-stu-id="6d3d3-177">The Task Scheduler Service is not running.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6d3d3-178"><span id="SCHED_E_UNEXPECTEDNODE"></span><span id="sched_e_unexpectednode"></span>**已計畫的 \_ 電子 \_ UNEXPECTEDNODE**</span><span class="sxs-lookup"><span data-stu-id="6d3d3-178"><span id="SCHED_E_UNEXPECTEDNODE"></span><span id="sched_e_unexpectednode"></span>**SCHED\_E\_UNEXPECTEDNODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d3d3-179">0x80041316</span><span class="sxs-lookup"><span data-stu-id="6d3d3-179">0x80041316</span></span>
</dt> <dt>



<span data-ttu-id="6d3d3-180">工作 XML 包含未預期的節點。</span><span class="sxs-lookup"><span data-stu-id="6d3d3-180">The task XML contains an unexpected node.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6d3d3-181"><span id="SCHED_E_NAMESPACE"></span><span id="sched_e_namespace"></span>**已計畫的 \_ 電子 \_ 命名空間**</span><span class="sxs-lookup"><span data-stu-id="6d3d3-181"><span id="SCHED_E_NAMESPACE"></span><span id="sched_e_namespace"></span>**SCHED\_E\_NAMESPACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d3d3-182">0x80041317</span><span class="sxs-lookup"><span data-stu-id="6d3d3-182">0x80041317</span></span>
</dt> <dt>



<span data-ttu-id="6d3d3-183">工作 XML 包含非預期命名空間中的元素或屬性。</span><span class="sxs-lookup"><span data-stu-id="6d3d3-183">The task XML contains an element or attribute from an unexpected namespace.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6d3d3-184"><span id="SCHED_E_INVALIDVALUE"></span><span id="sched_e_invalidvalue"></span>**已計畫的 \_ 電子 \_ INVALIDVALUE**</span><span class="sxs-lookup"><span data-stu-id="6d3d3-184"><span id="SCHED_E_INVALIDVALUE"></span><span id="sched_e_invalidvalue"></span>**SCHED\_E\_INVALIDVALUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d3d3-185">0x80041318</span><span class="sxs-lookup"><span data-stu-id="6d3d3-185">0x80041318</span></span>
</dt> <dt>



<span data-ttu-id="6d3d3-186">工作 XML 包含格式不正確或超出範圍的值。</span><span class="sxs-lookup"><span data-stu-id="6d3d3-186">The task XML contains a value which is incorrectly formatted or out of range.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6d3d3-187"><span id="SCHED_E_MISSINGNODE"></span><span id="sched_e_missingnode"></span>**已計畫的 \_ 電子 \_ MISSINGNODE**</span><span class="sxs-lookup"><span data-stu-id="6d3d3-187"><span id="SCHED_E_MISSINGNODE"></span><span id="sched_e_missingnode"></span>**SCHED\_E\_MISSINGNODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d3d3-188">0x80041319</span><span class="sxs-lookup"><span data-stu-id="6d3d3-188">0x80041319</span></span>
</dt> <dt>



<span data-ttu-id="6d3d3-189">工作 XML 缺少必要的元素或屬性。</span><span class="sxs-lookup"><span data-stu-id="6d3d3-189">The task XML is missing a required element or attribute.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6d3d3-190"><span id="SCHED_E_MALFORMEDXML"></span><span id="sched_e_malformedxml"></span>**已計畫的 \_ 電子 \_ MALFORMEDXML**</span><span class="sxs-lookup"><span data-stu-id="6d3d3-190"><span id="SCHED_E_MALFORMEDXML"></span><span id="sched_e_malformedxml"></span>**SCHED\_E\_MALFORMEDXML**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d3d3-191">0x8004131A</span><span class="sxs-lookup"><span data-stu-id="6d3d3-191">0x8004131A</span></span>
</dt> <dt>



<span data-ttu-id="6d3d3-192">工作 XML 的格式不正確。</span><span class="sxs-lookup"><span data-stu-id="6d3d3-192">The task XML is malformed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6d3d3-193"><span id="SCHED_S_SOME_TRIGGERS_FAILED"></span><span id="sched_s_some_triggers_failed"></span>**已計畫的 \_ \_ 部分 \_ 觸發程式 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="6d3d3-193"><span id="SCHED_S_SOME_TRIGGERS_FAILED"></span><span id="sched_s_some_triggers_failed"></span>**SCHED\_S\_SOME\_TRIGGERS\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d3d3-194">0x0004131B</span><span class="sxs-lookup"><span data-stu-id="6d3d3-194">0x0004131B</span></span>
</dt> <dt>



<span data-ttu-id="6d3d3-195">工作已註冊，但並非所有指定的觸發程式都會啟動工作。</span><span class="sxs-lookup"><span data-stu-id="6d3d3-195">The task is registered, but not all specified triggers will start the task.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6d3d3-196"><span id="SCHED_S_BATCH_LOGON_PROBLEM"></span><span id="sched_s_batch_logon_problem"></span>**已計畫的 \_ \_ 批次 \_ 登入 \_ 問題**</span><span class="sxs-lookup"><span data-stu-id="6d3d3-196"><span id="SCHED_S_BATCH_LOGON_PROBLEM"></span><span id="sched_s_batch_logon_problem"></span>**SCHED\_S\_BATCH\_LOGON\_PROBLEM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d3d3-197">0x0004131C</span><span class="sxs-lookup"><span data-stu-id="6d3d3-197">0x0004131C</span></span>
</dt> <dt>



<span data-ttu-id="6d3d3-198">工作已註冊，但可能無法啟動。</span><span class="sxs-lookup"><span data-stu-id="6d3d3-198">The task is registered, but may fail to start.</span></span> <span data-ttu-id="6d3d3-199">必須啟用工作主體的批次登入許可權。</span><span class="sxs-lookup"><span data-stu-id="6d3d3-199">Batch logon privilege needs to be enabled for the task principal.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6d3d3-200"><span id="SCHED_E_TOO_MANY_NODES"></span><span id="sched_e_too_many_nodes"></span>**已計畫的 \_ 電子 \_ \_ 節點太多 \_**</span><span class="sxs-lookup"><span data-stu-id="6d3d3-200"><span id="SCHED_E_TOO_MANY_NODES"></span><span id="sched_e_too_many_nodes"></span>**SCHED\_E\_TOO\_MANY\_NODES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d3d3-201">0x8004131D</span><span class="sxs-lookup"><span data-stu-id="6d3d3-201">0x8004131D</span></span>
</dt> <dt>



<span data-ttu-id="6d3d3-202">工作 XML 包含太多相同型別的節點。</span><span class="sxs-lookup"><span data-stu-id="6d3d3-202">The task XML contains too many nodes of the same type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6d3d3-203"><span id="SCHED_E_PAST_END_BOUNDARY"></span><span id="sched_e_past_end_boundary"></span>**已計畫 \_ E \_ 超過 \_ 結束 \_ 界限**</span><span class="sxs-lookup"><span data-stu-id="6d3d3-203"><span id="SCHED_E_PAST_END_BOUNDARY"></span><span id="sched_e_past_end_boundary"></span>**SCHED\_E\_PAST\_END\_BOUNDARY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d3d3-204">0x8004131E</span><span class="sxs-lookup"><span data-stu-id="6d3d3-204">0x8004131E</span></span>
</dt> <dt>



<span data-ttu-id="6d3d3-205">工作無法在觸發程式結束界限之後啟動。</span><span class="sxs-lookup"><span data-stu-id="6d3d3-205">The task cannot be started after the trigger end boundary.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6d3d3-206"><span id="SCHED_E_ALREADY_RUNNING"></span><span id="sched_e_already_running"></span>**已計畫的 \_ 電子郵件 \_ 已在執行中 \_**</span><span class="sxs-lookup"><span data-stu-id="6d3d3-206"><span id="SCHED_E_ALREADY_RUNNING"></span><span id="sched_e_already_running"></span>**SCHED\_E\_ALREADY\_RUNNING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d3d3-207">0x8004131F</span><span class="sxs-lookup"><span data-stu-id="6d3d3-207">0x8004131F</span></span>
</dt> <dt>



<span data-ttu-id="6d3d3-208">這項工作的實例已經在執行。</span><span class="sxs-lookup"><span data-stu-id="6d3d3-208">An instance of this task is already running.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6d3d3-209"><span id="SCHED_E_USER_NOT_LOGGED_ON"></span><span id="sched_e_user_not_logged_on"></span>**\_已計畫 \_ 的電子使用者 \_ 未 \_ 登入 \_**</span><span class="sxs-lookup"><span data-stu-id="6d3d3-209"><span id="SCHED_E_USER_NOT_LOGGED_ON"></span><span id="sched_e_user_not_logged_on"></span>**SCHED\_E\_USER\_NOT\_LOGGED\_ON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d3d3-210">0x80041320</span><span class="sxs-lookup"><span data-stu-id="6d3d3-210">0x80041320</span></span>
</dt> <dt>



<span data-ttu-id="6d3d3-211">工作將不會執行，因為使用者未登入。</span><span class="sxs-lookup"><span data-stu-id="6d3d3-211">The task will not run because the user is not logged on.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6d3d3-212"><span id="SCHED_E_INVALID_TASK_HASH"></span><span id="sched_e_invalid_task_hash"></span>**已計畫 \_ 電子不正確工作 \_ \_ \_ 雜湊**</span><span class="sxs-lookup"><span data-stu-id="6d3d3-212"><span id="SCHED_E_INVALID_TASK_HASH"></span><span id="sched_e_invalid_task_hash"></span>**SCHED\_E\_INVALID\_TASK\_HASH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d3d3-213">0x80041321</span><span class="sxs-lookup"><span data-stu-id="6d3d3-213">0x80041321</span></span>
</dt> <dt>



<span data-ttu-id="6d3d3-214">工作映射已損毀或已遭篡改。</span><span class="sxs-lookup"><span data-stu-id="6d3d3-214">The task image is corrupt or has been tampered with.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6d3d3-215"><span id="SCHED_E_SERVICE_NOT_AVAILABLE"></span><span id="sched_e_service_not_available"></span>**已計畫的 \_ 電子 \_ 服務 \_ 無法 \_ 使用**</span><span class="sxs-lookup"><span data-stu-id="6d3d3-215"><span id="SCHED_E_SERVICE_NOT_AVAILABLE"></span><span id="sched_e_service_not_available"></span>**SCHED\_E\_SERVICE\_NOT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d3d3-216">0x80041322</span><span class="sxs-lookup"><span data-stu-id="6d3d3-216">0x80041322</span></span>
</dt> <dt>



<span data-ttu-id="6d3d3-217">工作排程器服務無法使用。</span><span class="sxs-lookup"><span data-stu-id="6d3d3-217">The Task Scheduler service is not available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6d3d3-218"><span id="SCHED_E_SERVICE_TOO_BUSY"></span><span id="sched_e_service_too_busy"></span>**已計畫的 \_ 電子 \_ 服務 \_ 太 \_ 忙碌**</span><span class="sxs-lookup"><span data-stu-id="6d3d3-218"><span id="SCHED_E_SERVICE_TOO_BUSY"></span><span id="sched_e_service_too_busy"></span>**SCHED\_E\_SERVICE\_TOO\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d3d3-219">0x80041323</span><span class="sxs-lookup"><span data-stu-id="6d3d3-219">0x80041323</span></span>
</dt> <dt>



<span data-ttu-id="6d3d3-220">工作排程器服務太忙碌，無法處理您的要求。</span><span class="sxs-lookup"><span data-stu-id="6d3d3-220">The Task Scheduler service is too busy to handle your request.</span></span> <span data-ttu-id="6d3d3-221">請稍後再試一次。</span><span class="sxs-lookup"><span data-stu-id="6d3d3-221">Please try again later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6d3d3-222"><span id="SCHED_E_TASK_ATTEMPTED"></span><span id="sched_e_task_attempted"></span>**已計畫的電子工作已 \_ \_ \_ 嘗試**</span><span class="sxs-lookup"><span data-stu-id="6d3d3-222"><span id="SCHED_E_TASK_ATTEMPTED"></span><span id="sched_e_task_attempted"></span>**SCHED\_E\_TASK\_ATTEMPTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d3d3-223">0x80041324</span><span class="sxs-lookup"><span data-stu-id="6d3d3-223">0x80041324</span></span>
</dt> <dt>



<span data-ttu-id="6d3d3-224">工作排程器服務嘗試執行此工作，但是工作定義中的其中一個條件約束，因此工作並未執行。</span><span class="sxs-lookup"><span data-stu-id="6d3d3-224">The Task Scheduler service attempted to run the task, but the task did not run due to one of the constraints in the task definition.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6d3d3-225"><span id="SCHED_S_TASK_QUEUED"></span><span id="sched_s_task_queued"></span>**已計畫的工作已 \_ \_ \_ 排入佇列**</span><span class="sxs-lookup"><span data-stu-id="6d3d3-225"><span id="SCHED_S_TASK_QUEUED"></span><span id="sched_s_task_queued"></span>**SCHED\_S\_TASK\_QUEUED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d3d3-226">0x00041325</span><span class="sxs-lookup"><span data-stu-id="6d3d3-226">0x00041325</span></span>
</dt> <dt>



<span data-ttu-id="6d3d3-227">工作排程器服務要求執行工作。</span><span class="sxs-lookup"><span data-stu-id="6d3d3-227">The Task Scheduler service has asked the task to run.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6d3d3-228"><span id="SCHED_E_TASK_DISABLED"></span><span id="sched_e_task_disabled"></span>**已計畫的 \_ 電子工作 \_ \_ 已停用**</span><span class="sxs-lookup"><span data-stu-id="6d3d3-228"><span id="SCHED_E_TASK_DISABLED"></span><span id="sched_e_task_disabled"></span>**SCHED\_E\_TASK\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d3d3-229">0x80041326</span><span class="sxs-lookup"><span data-stu-id="6d3d3-229">0x80041326</span></span>
</dt> <dt>



<span data-ttu-id="6d3d3-230">工作已停用。</span><span class="sxs-lookup"><span data-stu-id="6d3d3-230">The task is disabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6d3d3-231"><span id="SCHED_E_TASK_NOT_V1_COMPAT"></span><span id="sched_e_task_not_v1_compat"></span>**已計畫的 \_ 電子工作 \_ 不是 \_ \_ V1 \_ 相容性**</span><span class="sxs-lookup"><span data-stu-id="6d3d3-231"><span id="SCHED_E_TASK_NOT_V1_COMPAT"></span><span id="sched_e_task_not_v1_compat"></span>**SCHED\_E\_TASK\_NOT\_V1\_COMPAT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d3d3-232">0x80041327</span><span class="sxs-lookup"><span data-stu-id="6d3d3-232">0x80041327</span></span>
</dt> <dt>



<span data-ttu-id="6d3d3-233">此工作具有與舊版 Windows 不相容的屬性。</span><span class="sxs-lookup"><span data-stu-id="6d3d3-233">The task has properties that are not compatible with earlier versions of Windows.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6d3d3-234"><span id="SCHED_E_START_ON_DEMAND"></span><span id="sched_e_start_on_demand"></span>**依 \_ \_ 需求計畫 \_ 的 E 啟動 \_**</span><span class="sxs-lookup"><span data-stu-id="6d3d3-234"><span id="SCHED_E_START_ON_DEMAND"></span><span id="sched_e_start_on_demand"></span>**SCHED\_E\_START\_ON\_DEMAND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d3d3-235">0x80041328</span><span class="sxs-lookup"><span data-stu-id="6d3d3-235">0x80041328</span></span>
</dt> <dt>



<span data-ttu-id="6d3d3-236">工作設定不允許工作隨選啟動。</span><span class="sxs-lookup"><span data-stu-id="6d3d3-236">The task settings do not allow the task to start on demand.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6d3d3-237">規格需求</span><span class="sxs-lookup"><span data-stu-id="6d3d3-237">Requirements</span></span>



| <span data-ttu-id="6d3d3-238">需求</span><span class="sxs-lookup"><span data-stu-id="6d3d3-238">Requirement</span></span> | <span data-ttu-id="6d3d3-239">值</span><span class="sxs-lookup"><span data-stu-id="6d3d3-239">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6d3d3-240">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6d3d3-240">Minimum supported client</span></span><br/> | <span data-ttu-id="6d3d3-241">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6d3d3-241">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6d3d3-242">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6d3d3-242">Minimum supported server</span></span><br/> | <span data-ttu-id="6d3d3-243">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6d3d3-243">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6d3d3-244">標頭</span><span class="sxs-lookup"><span data-stu-id="6d3d3-244">Header</span></span><br/>                   | <dl> <span data-ttu-id="6d3d3-245"><dt>Winerror.h。h</dt></span><span class="sxs-lookup"><span data-stu-id="6d3d3-245"><dt>WinError.h</dt></span></span> </dl> |



 

 





