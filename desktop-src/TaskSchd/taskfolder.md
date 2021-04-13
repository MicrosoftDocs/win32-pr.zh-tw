---
title: TaskFolder 物件
description: 提供方法的腳本物件，此物件會提供用來註冊 (在資料夾中建立) 工作、從資料夾中移除工作，以及從資料夾建立或移除子資料夾的方法。
ms.assetid: f6fd09ec-2777-4903-83b5-e3ac1aa472a0
keywords:
- TaskFolder 物件工作排程器
- TaskFolder 物件工作排程器，說明
topic_type:
- apiref
api_name:
- TaskFolder
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1ccad9331cf3df12ea5752fdd7e5ac94bfbeba6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509123"
---
# <a name="taskfolder-object"></a><span data-ttu-id="050e1-105">TaskFolder 物件</span><span class="sxs-lookup"><span data-stu-id="050e1-105">TaskFolder object</span></span>

<span data-ttu-id="050e1-106">提供方法的腳本物件，此物件會提供用來註冊 (在資料夾中建立) 工作、從資料夾中移除工作，以及從資料夾建立或移除子資料夾的方法。</span><span class="sxs-lookup"><span data-stu-id="050e1-106">Scripting object that provides the methods that are used to register (create) tasks in the folder, remove tasks from the folder, and create or remove subfolders from the folder.</span></span>

## <a name="members"></a><span data-ttu-id="050e1-107">成員</span><span class="sxs-lookup"><span data-stu-id="050e1-107">Members</span></span>

<span data-ttu-id="050e1-108">**TaskFolder** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="050e1-108">The **TaskFolder** object has these types of members:</span></span>

-   [<span data-ttu-id="050e1-109">方法</span><span class="sxs-lookup"><span data-stu-id="050e1-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="050e1-110">屬性</span><span class="sxs-lookup"><span data-stu-id="050e1-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="050e1-111">方法</span><span class="sxs-lookup"><span data-stu-id="050e1-111">Methods</span></span>

<span data-ttu-id="050e1-112">**TaskFolder** 物件有這些方法。</span><span class="sxs-lookup"><span data-stu-id="050e1-112">The **TaskFolder** object has these methods.</span></span>



| <span data-ttu-id="050e1-113">方法</span><span class="sxs-lookup"><span data-stu-id="050e1-113">Method</span></span>                                                              | <span data-ttu-id="050e1-114">描述</span><span class="sxs-lookup"><span data-stu-id="050e1-114">Description</span></span>                                                                                                                                    |
|:--------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="050e1-115">**CreateFolder**</span><span class="sxs-lookup"><span data-stu-id="050e1-115">**CreateFolder**</span></span>](taskfolder-createfolder.md)                     | <span data-ttu-id="050e1-116">建立相關工作的資料夾。</span><span class="sxs-lookup"><span data-stu-id="050e1-116">Creates a folder for related tasks.</span></span><br/>                                                                                                 |
| [<span data-ttu-id="050e1-117">**DeleteFolder**</span><span class="sxs-lookup"><span data-stu-id="050e1-117">**DeleteFolder**</span></span>](taskfolder-deletefolder.md)                     | <span data-ttu-id="050e1-118">刪除父資料夾中的子資料夾。</span><span class="sxs-lookup"><span data-stu-id="050e1-118">Deletes a subfolder from the parent folder.</span></span><br/>                                                                                         |
| [<span data-ttu-id="050e1-119">**DeleteTask**</span><span class="sxs-lookup"><span data-stu-id="050e1-119">**DeleteTask**</span></span>](taskfolder-deletetask.md)                         | <span data-ttu-id="050e1-120">從資料夾刪除工作。</span><span class="sxs-lookup"><span data-stu-id="050e1-120">Deletes a task from the folder.</span></span><br/>                                                                                                     |
| [<span data-ttu-id="050e1-121">**GetFolder**</span><span class="sxs-lookup"><span data-stu-id="050e1-121">**GetFolder**</span></span>](taskfolder-getfolder.md)                           | <span data-ttu-id="050e1-122">取得資料夾，其中包含指定位置的工作。</span><span class="sxs-lookup"><span data-stu-id="050e1-122">Gets a folder that contains tasks at a specified location.</span></span><br/>                                                                          |
| [<span data-ttu-id="050e1-123">**GetFolders**</span><span class="sxs-lookup"><span data-stu-id="050e1-123">**GetFolders**</span></span>](taskfolder-getfolders.md)                         | <span data-ttu-id="050e1-124">取得資料夾中的所有子資料夾。</span><span class="sxs-lookup"><span data-stu-id="050e1-124">Gets all the subfolders in the folder.</span></span><br/>                                                                                              |
| [<span data-ttu-id="050e1-125">**GetSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="050e1-125">**GetSecurityDescriptor**</span></span>](taskfolder-getsecuritydescriptor.md)   | <span data-ttu-id="050e1-126">取得資料夾的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="050e1-126">Gets the security descriptor for the folder.</span></span><br/>                                                                                        |
| [<span data-ttu-id="050e1-127">**GetTask**</span><span class="sxs-lookup"><span data-stu-id="050e1-127">**GetTask**</span></span>](taskfolder-gettask.md)                               | <span data-ttu-id="050e1-128">取得資料夾中位於指定位置的工作。</span><span class="sxs-lookup"><span data-stu-id="050e1-128">Gets a task at a specified location in a folder.</span></span><br/>                                                                                    |
| [<span data-ttu-id="050e1-129">**GetTasks**</span><span class="sxs-lookup"><span data-stu-id="050e1-129">**GetTasks**</span></span>](taskfolder-gettasks.md)                             | <span data-ttu-id="050e1-130">取得資料夾中的所有工作。</span><span class="sxs-lookup"><span data-stu-id="050e1-130">Gets all the tasks in the folder.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="050e1-131">**RegisterTask**</span><span class="sxs-lookup"><span data-stu-id="050e1-131">**RegisterTask**</span></span>](taskfolder-registertask.md)                     | <span data-ttu-id="050e1-132">註冊 (會使用 XML 來定義工作，以在資料夾中建立) 新工作。</span><span class="sxs-lookup"><span data-stu-id="050e1-132">Registers (creates) a new task in the folder using XML to define the task.</span></span><br/>                                                          |
| [<span data-ttu-id="050e1-133">**RegisterTaskDefinition**</span><span class="sxs-lookup"><span data-stu-id="050e1-133">**RegisterTaskDefinition**</span></span>](taskfolder-registertaskdefinition.md) | <span data-ttu-id="050e1-134">註冊 (會使用 [**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) 介面來定義工作，以在指定的位置建立) 工作。</span><span class="sxs-lookup"><span data-stu-id="050e1-134">Registers (creates) a task in a specified location using the [**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) interface to define a task.</span></span><br/> |
| [<span data-ttu-id="050e1-135">**SetSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="050e1-135">**SetSecurityDescriptor**</span></span>](taskfolder-setsecuritydescriptor.md)   | <span data-ttu-id="050e1-136">設定資料夾的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="050e1-136">Sets the security descriptor for the folder.</span></span><br/>                                                                                        |



 

### <a name="properties"></a><span data-ttu-id="050e1-137">屬性</span><span class="sxs-lookup"><span data-stu-id="050e1-137">Properties</span></span>

<span data-ttu-id="050e1-138">**TaskFolder** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="050e1-138">The **TaskFolder** object has these properties.</span></span>



| <span data-ttu-id="050e1-139">屬性</span><span class="sxs-lookup"><span data-stu-id="050e1-139">Property</span></span>                                   | <span data-ttu-id="050e1-140">存取類型</span><span class="sxs-lookup"><span data-stu-id="050e1-140">Access type</span></span>          | <span data-ttu-id="050e1-141">Description</span><span class="sxs-lookup"><span data-stu-id="050e1-141">Description</span></span>                                                                        |
|:-------------------------------------------|:---------------------|:-----------------------------------------------------------------------------------|
| [<span data-ttu-id="050e1-142">**Name**</span><span class="sxs-lookup"><span data-stu-id="050e1-142">**Name**</span></span>](taskfolder-name.md)<br/> | <span data-ttu-id="050e1-143">唯讀</span><span class="sxs-lookup"><span data-stu-id="050e1-143">Read-only</span></span><br/> | <span data-ttu-id="050e1-144">取得用來識別包含工作之資料夾的名稱。</span><span class="sxs-lookup"><span data-stu-id="050e1-144">Gets the name that is used to identify the folder that contains a task.</span></span><br/> |
| [<span data-ttu-id="050e1-145">**路徑**</span><span class="sxs-lookup"><span data-stu-id="050e1-145">**Path**</span></span>](taskfolder-path.md)<br/> | <span data-ttu-id="050e1-146">唯讀</span><span class="sxs-lookup"><span data-stu-id="050e1-146">Read-only</span></span><br/> | <span data-ttu-id="050e1-147">取得儲存資料夾的路徑。</span><span class="sxs-lookup"><span data-stu-id="050e1-147">Gets the path to where the folder is stored.</span></span><br/>                            |



 

## <a name="examples"></a><span data-ttu-id="050e1-148">範例</span><span class="sxs-lookup"><span data-stu-id="050e1-148">Examples</span></span>

<span data-ttu-id="050e1-149">如需此腳本物件的詳細資訊和範例程式碼，請參閱[時間觸發程式範例 (腳本) ](time-trigger-example--scripting-.md)、[事件觸發程式範例 (腳本) ](https://www.bing.com/search?q=Event+Trigger+Example+(Scripting))、[每日觸發程式範例 (腳本](daily-trigger-example--scripting-.md)) 、[註冊觸發](registration-trigger-example--scripting-.md)程式範例 (腳本) 、[每週觸發](weekly-trigger-example--scripting-.md)程式範例 (腳本) 、[登入觸發](logon-trigger-example--scripting-.md)程式範例 (腳本) ，或顯示 (腳本[) 的工作](boot-trigger-example--scripting-.md)[名稱和狀態](displaying-task-names-and-state--scripting-.md)。</span><span class="sxs-lookup"><span data-stu-id="050e1-149">For more information and example code for this scripting object, see [Time Trigger Example (Scripting)](time-trigger-example--scripting-.md), [Event Trigger Example (Scripting)](https://www.bing.com/search?q=Event+Trigger+Example+(Scripting)), [Daily Trigger Example (Scripting)](daily-trigger-example--scripting-.md), [Registration Trigger Example (Scripting)](registration-trigger-example--scripting-.md), [Weekly Trigger Example (Scripting)](weekly-trigger-example--scripting-.md), [Logon Trigger Example (Scripting)](logon-trigger-example--scripting-.md), [Boot Trigger Example (Scripting)](boot-trigger-example--scripting-.md), or [Displaying Task Names and States (Scripting)](displaying-task-names-and-state--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="050e1-150">規格需求</span><span class="sxs-lookup"><span data-stu-id="050e1-150">Requirements</span></span>



| <span data-ttu-id="050e1-151">需求</span><span class="sxs-lookup"><span data-stu-id="050e1-151">Requirement</span></span> | <span data-ttu-id="050e1-152">值</span><span class="sxs-lookup"><span data-stu-id="050e1-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="050e1-153">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="050e1-153">Minimum supported client</span></span><br/> | <span data-ttu-id="050e1-154">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="050e1-154">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="050e1-155">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="050e1-155">Minimum supported server</span></span><br/> | <span data-ttu-id="050e1-156">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="050e1-156">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="050e1-157">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="050e1-157">Type library</span></span><br/>             | <dl> <span data-ttu-id="050e1-158"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="050e1-158"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="050e1-159">DLL</span><span class="sxs-lookup"><span data-stu-id="050e1-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="050e1-160"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="050e1-160"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="050e1-161">另請參閱</span><span class="sxs-lookup"><span data-stu-id="050e1-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="050e1-162">工作排程器物件</span><span class="sxs-lookup"><span data-stu-id="050e1-162">Task Scheduler Objects</span></span>](task-scheduler-objects.md)
</dt> <dt>

[<span data-ttu-id="050e1-163">工作排程器</span><span class="sxs-lookup"><span data-stu-id="050e1-163">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





