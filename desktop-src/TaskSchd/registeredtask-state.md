---
title: RegisteredTask。 State 屬性
description: 針對腳本，取得已註冊工作的操作狀態。
ms.assetid: 1acd4946-322f-4f24-b317-92be80e19de5
keywords:
- State 屬性工作排程器
- State 屬性工作排程器，RegisteredTask 物件
- RegisteredTask 物件工作排程器，State 屬性
topic_type:
- apiref
api_name:
- RegisteredTask.State
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47af082174bc6927a16760e87566f311ec9f4a14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466769"
---
# <a name="registeredtaskstate-property"></a><span data-ttu-id="911fd-106">RegisteredTask。 State 屬性</span><span class="sxs-lookup"><span data-stu-id="911fd-106">RegisteredTask.State property</span></span>

<span data-ttu-id="911fd-107">針對腳本，取得已註冊工作的操作狀態。</span><span class="sxs-lookup"><span data-stu-id="911fd-107">For scripting, gets the operational state of the registered task.</span></span>

## <a name="syntax"></a><span data-ttu-id="911fd-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="911fd-108">Syntax</span></span>


```VB
RegisteredTask.State As Integer
```



## <a name="property-value"></a><span data-ttu-id="911fd-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="911fd-109">Property value</span></span>

<span data-ttu-id="911fd-110">工作 [**\_ 狀態**](/windows/desktop/api/taskschd/ne-taskschd-task_state) 常數，定義工作的操作狀態。</span><span class="sxs-lookup"><span data-stu-id="911fd-110">A [**TASK\_STATE**](/windows/desktop/api/taskschd/ne-taskschd-task_state) constant that defines the operational state of the task.</span></span>



| <span data-ttu-id="911fd-111">值</span><span class="sxs-lookup"><span data-stu-id="911fd-111">Value</span></span>                                                                                                                                                                                                                                   | <span data-ttu-id="911fd-112">意義</span><span class="sxs-lookup"><span data-stu-id="911fd-112">Meaning</span></span>                                                                                                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_STATE_UNKNOWN"></span><span id="task_state_unknown"></span><dl> <span data-ttu-id="911fd-113"><dt>**工作 \_狀態 \_ 不明**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="911fd-113"><dt>**TASK\_STATE\_UNKNOWN**</dt> <dt>0</dt></span></span> </dl>    | <span data-ttu-id="911fd-114">工作的狀態未知。</span><span class="sxs-lookup"><span data-stu-id="911fd-114">The state of the task is unknown.</span></span><br/>                                                                                                      |
| <span id="TASK_STATE_DISABLED"></span><span id="task_state_disabled"></span><dl> <span data-ttu-id="911fd-115"><dt>**工作 \_\_停用狀態**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="911fd-115"><dt>**TASK\_STATE\_DISABLED**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="911fd-116">工作已註冊但已停用，而且沒有工作的實例已排入佇列或正在執行中。</span><span class="sxs-lookup"><span data-stu-id="911fd-116">The task is registered but is disabled and no instances of the task are queued or running.</span></span> <span data-ttu-id="911fd-117">工作必須等到啟用之後才能執行。</span><span class="sxs-lookup"><span data-stu-id="911fd-117">The task cannot be run until it is enabled.</span></span><br/> |
| <span id="TASK_STATE_QUEUED"></span><span id="task_state_queued"></span><dl> <span data-ttu-id="911fd-118"><dt>**工作 \_狀態已 \_ 排入佇列**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="911fd-118"><dt>**TASK\_STATE\_QUEUED**</dt> <dt>2</dt></span></span> </dl>       | <span data-ttu-id="911fd-119">工作的實例已排入佇列。</span><span class="sxs-lookup"><span data-stu-id="911fd-119">Instances of the task are queued.</span></span><br/>                                                                                                      |
| <span id="TASK_STATE_READY"></span><span id="task_state_ready"></span><dl> <span data-ttu-id="911fd-120"><dt>**工作 \_狀態 \_ 就緒**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="911fd-120"><dt>**TASK\_STATE\_READY**</dt> <dt>3</dt></span></span> </dl>          | <span data-ttu-id="911fd-121">工作已準備好執行，但沒有任何實例已排入佇列或正在執行中。</span><span class="sxs-lookup"><span data-stu-id="911fd-121">The task is ready to be executed, but no instances are queued or running.</span></span><br/>                                                              |
| <span id="TASK_STATE_RUNNING"></span><span id="task_state_running"></span><dl> <span data-ttu-id="911fd-122"><dt>**工作 \_執行 \_**</dt> <dt>4</dt>的狀態</span><span class="sxs-lookup"><span data-stu-id="911fd-122"><dt>**TASK\_STATE\_RUNNING**</dt> <dt>4</dt></span></span> </dl>    | <span data-ttu-id="911fd-123">工作的一或多個實例正在執行。</span><span class="sxs-lookup"><span data-stu-id="911fd-123">One or more instances of the task are running.</span></span><br/>                                                                                         |



 

## <a name="requirements"></a><span data-ttu-id="911fd-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="911fd-124">Requirements</span></span>



| <span data-ttu-id="911fd-125">需求</span><span class="sxs-lookup"><span data-stu-id="911fd-125">Requirement</span></span> | <span data-ttu-id="911fd-126">值</span><span class="sxs-lookup"><span data-stu-id="911fd-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="911fd-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="911fd-127">Minimum supported client</span></span><br/> | <span data-ttu-id="911fd-128">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="911fd-128">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="911fd-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="911fd-129">Minimum supported server</span></span><br/> | <span data-ttu-id="911fd-130">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="911fd-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="911fd-131">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="911fd-131">Type library</span></span><br/>             | <dl> <span data-ttu-id="911fd-132"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="911fd-132"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="911fd-133">DLL</span><span class="sxs-lookup"><span data-stu-id="911fd-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="911fd-134"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="911fd-134"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="911fd-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="911fd-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="911fd-136">工作排程器</span><span class="sxs-lookup"><span data-stu-id="911fd-136">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="911fd-137">**RegisteredTask**</span><span class="sxs-lookup"><span data-stu-id="911fd-137">**RegisteredTask**</span></span>](registeredtask.md)
</dt> </dl>

 

 





