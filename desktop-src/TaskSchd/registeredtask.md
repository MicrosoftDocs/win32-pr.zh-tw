---
title: RegisteredTask 物件
description: 腳本物件，提供用來立即執行工作的方法、取得工作的任何執行中實例、取得或設定用來註冊工作的認證，以及描述工作的屬性。
ms.assetid: d280f22b-4dd1-44df-be12-286fb1c029a3
keywords:
- RegisteredTask 物件工作排程器
- RegisteredTask 物件工作排程器，說明
topic_type:
- apiref
api_name:
- RegisteredTask
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7ce300375e5122a7b63266c0cd21cdddf34606b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685650"
---
# <a name="registeredtask-object"></a><span data-ttu-id="d6371-105">RegisteredTask 物件</span><span class="sxs-lookup"><span data-stu-id="d6371-105">RegisteredTask object</span></span>

<span data-ttu-id="d6371-106">腳本物件，提供用來立即執行工作的方法、取得工作的任何執行中實例、取得或設定用來註冊工作的認證，以及描述工作的屬性。</span><span class="sxs-lookup"><span data-stu-id="d6371-106">Scripting object that provides the methods that are used to run the task immediately, get any running instances of the task, get or set the credentials that are used to register the task, and the properties that describe the task.</span></span>

## <a name="members"></a><span data-ttu-id="d6371-107">成員</span><span class="sxs-lookup"><span data-stu-id="d6371-107">Members</span></span>

<span data-ttu-id="d6371-108">**RegisteredTask** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="d6371-108">The **RegisteredTask** object has these types of members:</span></span>

-   [<span data-ttu-id="d6371-109">方法</span><span class="sxs-lookup"><span data-stu-id="d6371-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="d6371-110">屬性</span><span class="sxs-lookup"><span data-stu-id="d6371-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="d6371-111">方法</span><span class="sxs-lookup"><span data-stu-id="d6371-111">Methods</span></span>

<span data-ttu-id="d6371-112">**RegisteredTask** 物件有這些方法。</span><span class="sxs-lookup"><span data-stu-id="d6371-112">The **RegisteredTask** object has these methods.</span></span>



| <span data-ttu-id="d6371-113">方法</span><span class="sxs-lookup"><span data-stu-id="d6371-113">Method</span></span>                                                                | <span data-ttu-id="d6371-114">描述</span><span class="sxs-lookup"><span data-stu-id="d6371-114">Description</span></span>                                                                                     |
|:----------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d6371-115">**GetInstances**</span><span class="sxs-lookup"><span data-stu-id="d6371-115">**GetInstances**</span></span>](registeredtask-getinstances.md)                   | <span data-ttu-id="d6371-116">傳回目前正在執行之已註冊工作的所有實例。</span><span class="sxs-lookup"><span data-stu-id="d6371-116">Returns all instances of the registered task that are currently running.</span></span><br/>             |
| [<span data-ttu-id="d6371-117">**GetRunTimes**</span><span class="sxs-lookup"><span data-stu-id="d6371-117">**GetRunTimes**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-getruntimes)                    | <span data-ttu-id="d6371-118">取得已註冊的工作排定在指定時間執行的時間。</span><span class="sxs-lookup"><span data-stu-id="d6371-118">Gets the times that the registered task is scheduled to run during a specified time.</span></span><br/> |
| [<span data-ttu-id="d6371-119">**GetSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="d6371-119">**GetSecurityDescriptor**</span></span>](registeredtask-getsecuritydescriptor.md) | <span data-ttu-id="d6371-120">取得用來做為已註冊工作之認證的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="d6371-120">Gets the security descriptor that is used as credentials for the registered task.</span></span><br/>    |
| [<span data-ttu-id="d6371-121">**執行**</span><span class="sxs-lookup"><span data-stu-id="d6371-121">**Run**</span></span>](registeredtask-run.md)                                     | <span data-ttu-id="d6371-122">立即執行已註冊的工作。</span><span class="sxs-lookup"><span data-stu-id="d6371-122">Runs the registered task immediately.</span></span><br/>                                                |
| [<span data-ttu-id="d6371-123">**RunEx**</span><span class="sxs-lookup"><span data-stu-id="d6371-123">**RunEx**</span></span>](registeredtask-runex.md)                                 | <span data-ttu-id="d6371-124">使用指定的旗標和會話識別碼，立即執行已註冊的工作。</span><span class="sxs-lookup"><span data-stu-id="d6371-124">Runs the registered task immediately using specified flags and a session identifier.</span></span><br/> |
| [<span data-ttu-id="d6371-125">**SetSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="d6371-125">**SetSecurityDescriptor**</span></span>](registeredtask-setsecuritydescriptor.md) | <span data-ttu-id="d6371-126">設定用來作為已註冊工作認證的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="d6371-126">Sets the security descriptor that is used as credentials for the registered task.</span></span><br/>    |
| [<span data-ttu-id="d6371-127">**停止**</span><span class="sxs-lookup"><span data-stu-id="d6371-127">**Stop**</span></span>](registeredtask-stop.md)                                   | <span data-ttu-id="d6371-128">立即停止已註冊的工作。</span><span class="sxs-lookup"><span data-stu-id="d6371-128">Stops the registered task immediately.</span></span><br/>                                               |



 

### <a name="properties"></a><span data-ttu-id="d6371-129">屬性</span><span class="sxs-lookup"><span data-stu-id="d6371-129">Properties</span></span>

<span data-ttu-id="d6371-130">**RegisteredTask** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="d6371-130">The **RegisteredTask** object has these properties.</span></span>



| <span data-ttu-id="d6371-131">屬性</span><span class="sxs-lookup"><span data-stu-id="d6371-131">Property</span></span>                                                                   | <span data-ttu-id="d6371-132">存取類型</span><span class="sxs-lookup"><span data-stu-id="d6371-132">Access type</span></span>           | <span data-ttu-id="d6371-133">Description</span><span class="sxs-lookup"><span data-stu-id="d6371-133">Description</span></span>                                                                               |
|:---------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d6371-134">**定義**</span><span class="sxs-lookup"><span data-stu-id="d6371-134">**Definition**</span></span>](registeredtask-definition.md)<br/>                 | <span data-ttu-id="d6371-135">唯讀</span><span class="sxs-lookup"><span data-stu-id="d6371-135">Read-only</span></span><br/>  | <span data-ttu-id="d6371-136">取得工作的定義。</span><span class="sxs-lookup"><span data-stu-id="d6371-136">Gets the definition of the task.</span></span><br/>                                               |
| [<span data-ttu-id="d6371-137">**啟用**</span><span class="sxs-lookup"><span data-stu-id="d6371-137">**Enabled**</span></span>](registeredtask-enabled.md)<br/>                       | <span data-ttu-id="d6371-138">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="d6371-138">Read/write</span></span><br/> | <span data-ttu-id="d6371-139">取得或設定布林值，這個值會指出是否已啟用註冊的工作。</span><span class="sxs-lookup"><span data-stu-id="d6371-139">Gets or set a Boolean value that indicates if the registered task is enabled.</span></span><br/>  |
| [<span data-ttu-id="d6371-140">**LastRunTime**</span><span class="sxs-lookup"><span data-stu-id="d6371-140">**LastRunTime**</span></span>](registeredtask-lastruntime.md)<br/>               | <span data-ttu-id="d6371-141">唯讀</span><span class="sxs-lookup"><span data-stu-id="d6371-141">Read-only</span></span><br/>  | <span data-ttu-id="d6371-142">取得上次執行註冊工作的時間。</span><span class="sxs-lookup"><span data-stu-id="d6371-142">Gets the time the registered task was last run.</span></span><br/>                                |
| [<span data-ttu-id="d6371-143">**LastTaskResult**</span><span class="sxs-lookup"><span data-stu-id="d6371-143">**LastTaskResult**</span></span>](registeredtask-lasttaskresult.md)<br/>         | <span data-ttu-id="d6371-144">唯讀</span><span class="sxs-lookup"><span data-stu-id="d6371-144">Read-only</span></span><br/>  | <span data-ttu-id="d6371-145">取得上次執行註冊工作時所傳回的結果。</span><span class="sxs-lookup"><span data-stu-id="d6371-145">Gets the results that were returned the last time the registered task was run.</span></span><br/> |
| [<span data-ttu-id="d6371-146">**Name**</span><span class="sxs-lookup"><span data-stu-id="d6371-146">**Name**</span></span>](registeredtask-name.md)<br/>                             | <span data-ttu-id="d6371-147">唯讀</span><span class="sxs-lookup"><span data-stu-id="d6371-147">Read-only</span></span><br/>  | <span data-ttu-id="d6371-148">取得已註冊工作的名稱。</span><span class="sxs-lookup"><span data-stu-id="d6371-148">Gets the name of the registered task.</span></span><br/>                                          |
| [<span data-ttu-id="d6371-149">**NextRunTime**</span><span class="sxs-lookup"><span data-stu-id="d6371-149">**NextRunTime**</span></span>](registeredtask-nextruntime.md)<br/>               | <span data-ttu-id="d6371-150">唯讀</span><span class="sxs-lookup"><span data-stu-id="d6371-150">Read-only</span></span><br/>  | <span data-ttu-id="d6371-151">取得已註冊的工作下次排程執行的時間。</span><span class="sxs-lookup"><span data-stu-id="d6371-151">Gets the time when the registered task is next scheduled to run.</span></span><br/>               |
| [<span data-ttu-id="d6371-152">**NumberOfMissedRuns**</span><span class="sxs-lookup"><span data-stu-id="d6371-152">**NumberOfMissedRuns**</span></span>](registeredtask-numberofmissedruns.md)<br/> | <span data-ttu-id="d6371-153">唯讀</span><span class="sxs-lookup"><span data-stu-id="d6371-153">Read-only</span></span><br/>  | <span data-ttu-id="d6371-154">取得已註冊的工作已錯過排程執行的次數。</span><span class="sxs-lookup"><span data-stu-id="d6371-154">Gets the number of times the registered task has missed a scheduled run.</span></span><br/>       |
| [<span data-ttu-id="d6371-155">**路徑**</span><span class="sxs-lookup"><span data-stu-id="d6371-155">**Path**</span></span>](registeredtask-path.md)<br/>                             | <span data-ttu-id="d6371-156">唯讀</span><span class="sxs-lookup"><span data-stu-id="d6371-156">Read-only</span></span><br/>  | <span data-ttu-id="d6371-157">取得已註冊的工作儲存位置的路徑。</span><span class="sxs-lookup"><span data-stu-id="d6371-157">Gets the path to where the registered task is stored.</span></span><br/>                          |
| [<span data-ttu-id="d6371-158">**狀態**</span><span class="sxs-lookup"><span data-stu-id="d6371-158">**State**</span></span>](registeredtask-state.md)<br/>                           | <span data-ttu-id="d6371-159">唯讀</span><span class="sxs-lookup"><span data-stu-id="d6371-159">Read-only</span></span><br/>  | <span data-ttu-id="d6371-160">取得已註冊工作的操作狀態。</span><span class="sxs-lookup"><span data-stu-id="d6371-160">Gets the operational state of the registered task.</span></span><br/>                             |
| [<span data-ttu-id="d6371-161">**XML**</span><span class="sxs-lookup"><span data-stu-id="d6371-161">**XML**</span></span>](registeredtask-xml.md)<br/>                               | <span data-ttu-id="d6371-162">唯讀</span><span class="sxs-lookup"><span data-stu-id="d6371-162">Read-only</span></span><br/>  | <span data-ttu-id="d6371-163">取得已註冊工作的 XML 格式註冊資訊。</span><span class="sxs-lookup"><span data-stu-id="d6371-163">Gets the XML-formatted registration information for the registered task.</span></span><br/>       |



 

## <a name="examples"></a><span data-ttu-id="d6371-164">範例</span><span class="sxs-lookup"><span data-stu-id="d6371-164">Examples</span></span>

<span data-ttu-id="d6371-165">如需此腳本物件的詳細資訊和範例程式碼，請參閱 [時間觸發程式範例 (腳本) ](time-trigger-example--scripting-.md) ，以及 [顯示 (腳本) 的工作名稱和狀態 ](displaying-task-names-and-state--scripting-.md)。</span><span class="sxs-lookup"><span data-stu-id="d6371-165">For more information and example code for this scripting object, see [Time Trigger Example (Scripting)](time-trigger-example--scripting-.md) and [Displaying Task Names and States (Scripting)](displaying-task-names-and-state--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d6371-166">規格需求</span><span class="sxs-lookup"><span data-stu-id="d6371-166">Requirements</span></span>



| <span data-ttu-id="d6371-167">需求</span><span class="sxs-lookup"><span data-stu-id="d6371-167">Requirement</span></span> | <span data-ttu-id="d6371-168">值</span><span class="sxs-lookup"><span data-stu-id="d6371-168">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d6371-169">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d6371-169">Minimum supported client</span></span><br/> | <span data-ttu-id="d6371-170">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d6371-170">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="d6371-171">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d6371-171">Minimum supported server</span></span><br/> | <span data-ttu-id="d6371-172">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d6371-172">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d6371-173">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="d6371-173">Type library</span></span><br/>             | <dl> <span data-ttu-id="d6371-174"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d6371-174"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d6371-175">DLL</span><span class="sxs-lookup"><span data-stu-id="d6371-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d6371-176"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d6371-176"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





