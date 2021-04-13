---
title: RunningTask 物件
description: 提供方法的腳本物件，這些方法可從執行中的工作取得資訊及控制其運作方式。
ms.assetid: 335e69d8-affa-4845-a067-641184e0f7df
keywords:
- RunningTask 物件工作排程器
- RunningTask 物件工作排程器，說明
topic_type:
- apiref
api_name:
- RunningTask
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 261be07f71d0d35f5d3140de1b39574b635a531e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508863"
---
# <a name="runningtask-object"></a><span data-ttu-id="3a0c8-105">RunningTask 物件</span><span class="sxs-lookup"><span data-stu-id="3a0c8-105">RunningTask object</span></span>

<span data-ttu-id="3a0c8-106">提供方法的腳本物件，這些方法可從執行中的工作取得資訊及控制其運作方式。</span><span class="sxs-lookup"><span data-stu-id="3a0c8-106">Scripting object that provides the methods to get information from and control a running task.</span></span>

## <a name="members"></a><span data-ttu-id="3a0c8-107">成員</span><span class="sxs-lookup"><span data-stu-id="3a0c8-107">Members</span></span>

<span data-ttu-id="3a0c8-108">**RunningTask** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="3a0c8-108">The **RunningTask** object has these types of members:</span></span>

-   [<span data-ttu-id="3a0c8-109">方法</span><span class="sxs-lookup"><span data-stu-id="3a0c8-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="3a0c8-110">屬性</span><span class="sxs-lookup"><span data-stu-id="3a0c8-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="3a0c8-111">方法</span><span class="sxs-lookup"><span data-stu-id="3a0c8-111">Methods</span></span>

<span data-ttu-id="3a0c8-112">**RunningTask** 物件有這些方法。</span><span class="sxs-lookup"><span data-stu-id="3a0c8-112">The **RunningTask** object has these methods.</span></span>



| <span data-ttu-id="3a0c8-113">方法</span><span class="sxs-lookup"><span data-stu-id="3a0c8-113">Method</span></span>                                 | <span data-ttu-id="3a0c8-114">描述</span><span class="sxs-lookup"><span data-stu-id="3a0c8-114">Description</span></span>                                                           |
|:---------------------------------------|:----------------------------------------------------------------------|
| [<span data-ttu-id="3a0c8-115">**重新整理**</span><span class="sxs-lookup"><span data-stu-id="3a0c8-115">**Refresh**</span></span>](runningtask-refresh.md) | <span data-ttu-id="3a0c8-116">重新整理工作的所有本機執行個體變數。</span><span class="sxs-lookup"><span data-stu-id="3a0c8-116">Refreshes all of the local instance variables of the task.</span></span><br/> |
| [<span data-ttu-id="3a0c8-117">**停止**</span><span class="sxs-lookup"><span data-stu-id="3a0c8-117">**Stop**</span></span>](runningtask-stop.md)       | <span data-ttu-id="3a0c8-118">停止此工作的實例。</span><span class="sxs-lookup"><span data-stu-id="3a0c8-118">Stops this instance of the task.</span></span><br/>                           |



 

### <a name="properties"></a><span data-ttu-id="3a0c8-119">屬性</span><span class="sxs-lookup"><span data-stu-id="3a0c8-119">Properties</span></span>

<span data-ttu-id="3a0c8-120">**RunningTask** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="3a0c8-120">The **RunningTask** object has these properties.</span></span>



| <span data-ttu-id="3a0c8-121">屬性</span><span class="sxs-lookup"><span data-stu-id="3a0c8-121">Property</span></span>                                                      | <span data-ttu-id="3a0c8-122">存取類型</span><span class="sxs-lookup"><span data-stu-id="3a0c8-122">Access type</span></span>          | <span data-ttu-id="3a0c8-123">Description</span><span class="sxs-lookup"><span data-stu-id="3a0c8-123">Description</span></span>                                                                         |
|:--------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------|
| [<span data-ttu-id="3a0c8-124">**CurrentAction**</span><span class="sxs-lookup"><span data-stu-id="3a0c8-124">**CurrentAction**</span></span>](runningtask-currentaction.md)<br/> | <span data-ttu-id="3a0c8-125">唯讀</span><span class="sxs-lookup"><span data-stu-id="3a0c8-125">Read-only</span></span><br/> | <span data-ttu-id="3a0c8-126">取得正在執行之工作正在執行之目前動作的名稱。</span><span class="sxs-lookup"><span data-stu-id="3a0c8-126">Gets the name of the current action that the running task is performing.</span></span><br/> |
| [<span data-ttu-id="3a0c8-127">**EnginePID**</span><span class="sxs-lookup"><span data-stu-id="3a0c8-127">**EnginePID**</span></span>](runningtask-enginepid.md)<br/>         | <span data-ttu-id="3a0c8-128">唯讀</span><span class="sxs-lookup"><span data-stu-id="3a0c8-128">Read-only</span></span><br/> | <span data-ttu-id="3a0c8-129">取得正在執行工作之引擎 (進程) 的處理序識別碼。</span><span class="sxs-lookup"><span data-stu-id="3a0c8-129">Gets the process ID for the engine (process) which is running the task.</span></span><br/>  |
| [<span data-ttu-id="3a0c8-130">**InstanceGuid**</span><span class="sxs-lookup"><span data-stu-id="3a0c8-130">**InstanceGuid**</span></span>](runningtask-instanceguid.md)<br/>   | <span data-ttu-id="3a0c8-131">唯讀</span><span class="sxs-lookup"><span data-stu-id="3a0c8-131">Read-only</span></span><br/> | <span data-ttu-id="3a0c8-132">取得此工作實例的 GUID 識別碼。</span><span class="sxs-lookup"><span data-stu-id="3a0c8-132">Gets the GUID identifier for this instance of the task.</span></span><br/>                  |
| [<span data-ttu-id="3a0c8-133">**Name**</span><span class="sxs-lookup"><span data-stu-id="3a0c8-133">**Name**</span></span>](runningtask-name.md)<br/>                   | <span data-ttu-id="3a0c8-134">唯讀</span><span class="sxs-lookup"><span data-stu-id="3a0c8-134">Read-only</span></span><br/> | <span data-ttu-id="3a0c8-135">取得工作的名稱。</span><span class="sxs-lookup"><span data-stu-id="3a0c8-135">Gets the name of the task.</span></span><br/>                                               |
| [<span data-ttu-id="3a0c8-136">**路徑**</span><span class="sxs-lookup"><span data-stu-id="3a0c8-136">**Path**</span></span>](runningtask-path.md)<br/>                   | <span data-ttu-id="3a0c8-137">唯讀</span><span class="sxs-lookup"><span data-stu-id="3a0c8-137">Read-only</span></span><br/> | <span data-ttu-id="3a0c8-138">取得工作儲存位置的路徑。</span><span class="sxs-lookup"><span data-stu-id="3a0c8-138">Gets the path to where the task is stored.</span></span><br/>                               |
| [<span data-ttu-id="3a0c8-139">**狀態**</span><span class="sxs-lookup"><span data-stu-id="3a0c8-139">**State**</span></span>](runningtask-state.md)<br/>                 | <span data-ttu-id="3a0c8-140">唯讀</span><span class="sxs-lookup"><span data-stu-id="3a0c8-140">Read-only</span></span><br/> | <span data-ttu-id="3a0c8-141">取得正在執行之工作的狀態。</span><span class="sxs-lookup"><span data-stu-id="3a0c8-141">Gets the state of the running task.</span></span> <br/>                                     |



 

## <a name="requirements"></a><span data-ttu-id="3a0c8-142">規格需求</span><span class="sxs-lookup"><span data-stu-id="3a0c8-142">Requirements</span></span>



| <span data-ttu-id="3a0c8-143">需求</span><span class="sxs-lookup"><span data-stu-id="3a0c8-143">Requirement</span></span> | <span data-ttu-id="3a0c8-144">值</span><span class="sxs-lookup"><span data-stu-id="3a0c8-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3a0c8-145">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3a0c8-145">Minimum supported client</span></span><br/> | <span data-ttu-id="3a0c8-146">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3a0c8-146">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="3a0c8-147">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3a0c8-147">Minimum supported server</span></span><br/> | <span data-ttu-id="3a0c8-148">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3a0c8-148">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3a0c8-149">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="3a0c8-149">Type library</span></span><br/>             | <dl> <span data-ttu-id="3a0c8-150"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="3a0c8-150"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="3a0c8-151">DLL</span><span class="sxs-lookup"><span data-stu-id="3a0c8-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3a0c8-152"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3a0c8-152"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a0c8-153">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3a0c8-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a0c8-154">工作排程器物件</span><span class="sxs-lookup"><span data-stu-id="3a0c8-154">Task Scheduler Objects</span></span>](task-scheduler-objects.md)
</dt> <dt>

[<span data-ttu-id="3a0c8-155">工作排程器</span><span class="sxs-lookup"><span data-stu-id="3a0c8-155">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="3a0c8-156">**RunningTaskCollection**</span><span class="sxs-lookup"><span data-stu-id="3a0c8-156">**RunningTaskCollection**</span></span>](runningtaskcollection.md)
</dt> <dt>

[<span data-ttu-id="3a0c8-157">**RegisteredTask。執行**</span><span class="sxs-lookup"><span data-stu-id="3a0c8-157">**RegisteredTask.Run**</span></span>](registeredtask-run.md)
</dt> <dt>

[<span data-ttu-id="3a0c8-158">**RegisteredTask.RunEx**</span><span class="sxs-lookup"><span data-stu-id="3a0c8-158">**RegisteredTask.RunEx**</span></span>](registeredtask-runex.md)
</dt> </dl>

 

 





