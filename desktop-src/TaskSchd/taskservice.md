---
title: TaskService 物件
description: 針對腳本，提供存取工作排程器服務來管理已註冊的工作。
ms.assetid: 6ddd43dc-d027-4792-a53b-07fe4d4a3576
keywords:
- TaskService 物件工作排程器
- TaskService 物件工作排程器，說明
topic_type:
- apiref
api_name:
- TaskService
- HighestVersion
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 762cd2445c3c6b720bba0f01ae48b787abc1fb38
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466412"
---
# <a name="taskservice-object"></a><span data-ttu-id="15cab-105">TaskService 物件</span><span class="sxs-lookup"><span data-stu-id="15cab-105">TaskService object</span></span>

<span data-ttu-id="15cab-106">針對腳本，提供存取工作排程器服務來管理已註冊的工作。</span><span class="sxs-lookup"><span data-stu-id="15cab-106">For scripting, provides access to the Task Scheduler service for managing registered tasks.</span></span>

<span data-ttu-id="15cab-107">在呼叫任何其他 **TaskService** 方法之前，應該先呼叫 [**TaskService**](taskservice-connect.md)方法。</span><span class="sxs-lookup"><span data-stu-id="15cab-107">The [**TaskService.Connect**](taskservice-connect.md) method should be called before calling any of the other **TaskService** methods.</span></span>

## <a name="members"></a><span data-ttu-id="15cab-108">成員</span><span class="sxs-lookup"><span data-stu-id="15cab-108">Members</span></span>

<span data-ttu-id="15cab-109">**TaskService** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="15cab-109">The **TaskService** object has these types of members:</span></span>

-   [<span data-ttu-id="15cab-110">方法</span><span class="sxs-lookup"><span data-stu-id="15cab-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="15cab-111">屬性</span><span class="sxs-lookup"><span data-stu-id="15cab-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="15cab-112">方法</span><span class="sxs-lookup"><span data-stu-id="15cab-112">Methods</span></span>

<span data-ttu-id="15cab-113">**TaskService** 物件有這些方法。</span><span class="sxs-lookup"><span data-stu-id="15cab-113">The **TaskService** object has these methods.</span></span>



| <span data-ttu-id="15cab-114">方法</span><span class="sxs-lookup"><span data-stu-id="15cab-114">Method</span></span>                                                 | <span data-ttu-id="15cab-115">描述</span><span class="sxs-lookup"><span data-stu-id="15cab-115">Description</span></span>                                                                                                                                                                                                          |
|:-------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="15cab-116">**連接**</span><span class="sxs-lookup"><span data-stu-id="15cab-116">**Connect**</span></span>](taskservice-connect.md)                 | <span data-ttu-id="15cab-117">連接至遠端電腦，並將此介面上的所有後續呼叫與遠端會話產生關聯。</span><span class="sxs-lookup"><span data-stu-id="15cab-117">Connects to a remote machine and associates all subsequent calls on this interface with a remote session.</span></span><br/>                                                                                                 |
| [<span data-ttu-id="15cab-118">**GetFolder**</span><span class="sxs-lookup"><span data-stu-id="15cab-118">**GetFolder**</span></span>](taskservice-getfolder.md)             | <span data-ttu-id="15cab-119">取得已註冊工作的資料夾路徑。</span><span class="sxs-lookup"><span data-stu-id="15cab-119">Gets the path to a folder of registered tasks.</span></span><br/>                                                                                                                                                            |
| [<span data-ttu-id="15cab-120">**GetRunningTasks**</span><span class="sxs-lookup"><span data-stu-id="15cab-120">**GetRunningTasks**</span></span>](taskservice-getrunningtasks.md) | <span data-ttu-id="15cab-121">取得正在執行之工作的集合。</span><span class="sxs-lookup"><span data-stu-id="15cab-121">Gets a collection of running tasks.</span></span><br/>                                                                                                                                                                       |
| [<span data-ttu-id="15cab-122">**NewTask**</span><span class="sxs-lookup"><span data-stu-id="15cab-122">**NewTask**</span></span>](taskservice-newtask.md)                 | <span data-ttu-id="15cab-123">傳回要填入設定和屬性的空白工作定義物件，然後使用 [**TaskFolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) 方法進行註冊。</span><span class="sxs-lookup"><span data-stu-id="15cab-123">Returns an empty task definition object to be filled in with settings and properties and then registered using the [**TaskFolder.RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) method.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="15cab-124">屬性</span><span class="sxs-lookup"><span data-stu-id="15cab-124">Properties</span></span>

<span data-ttu-id="15cab-125">**TaskService** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="15cab-125">The **TaskService** object has these properties.</span></span>



| <span data-ttu-id="15cab-126">屬性</span><span class="sxs-lookup"><span data-stu-id="15cab-126">Property</span></span>                                                          | <span data-ttu-id="15cab-127">描述</span><span class="sxs-lookup"><span data-stu-id="15cab-127">Description</span></span>                                                                                                                 |
|:------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="15cab-128">**連線**</span><span class="sxs-lookup"><span data-stu-id="15cab-128">**Connected**</span></span>](taskservice-connected.md)<br/>             | <span data-ttu-id="15cab-129">取得布林值，指出您是否連接到工作排程器服務。</span><span class="sxs-lookup"><span data-stu-id="15cab-129">Gets a Boolean value that indicates if you are connected to the Task Scheduler service.</span></span><br/>                          |
| [<span data-ttu-id="15cab-130">**ConnectedDomain**</span><span class="sxs-lookup"><span data-stu-id="15cab-130">**ConnectedDomain**</span></span>](taskservice-connecteddomain.md)<br/> | <span data-ttu-id="15cab-131">取得 [**TargetServer**](taskservice-targetserver.md) 電腦所連接之網域的名稱。</span><span class="sxs-lookup"><span data-stu-id="15cab-131">Gets the name of the domain to which the [**TargetServer**](taskservice-targetserver.md) computer is connected.</span></span><br/> |
| [<span data-ttu-id="15cab-132">**>connecteduser**</span><span class="sxs-lookup"><span data-stu-id="15cab-132">**ConnectedUser**</span></span>](taskservice-connecteduser.md)<br/>     | <span data-ttu-id="15cab-133">取得連接到工作排程器服務之使用者的名稱。</span><span class="sxs-lookup"><span data-stu-id="15cab-133">Gets the name of the user that is connected to the Task Scheduler service.</span></span><br/>                                       |
| <span data-ttu-id="15cab-134">HighestVersion</span><span class="sxs-lookup"><span data-stu-id="15cab-134">HighestVersion</span></span><br/>                                         | <span data-ttu-id="15cab-135">取得電腦支援之工作排程器的最高版本。</span><span class="sxs-lookup"><span data-stu-id="15cab-135">Gets the highest version of Task Scheduler that a computer supports.</span></span><br/>                                             |
| [<span data-ttu-id="15cab-136">**TargetServer**</span><span class="sxs-lookup"><span data-stu-id="15cab-136">**TargetServer**</span></span>](taskservice-targetserver.md)<br/>       | <span data-ttu-id="15cab-137">取得正在執行使用者所連接之工作排程器服務的電腦名稱稱。</span><span class="sxs-lookup"><span data-stu-id="15cab-137">Gets the name of the computer that is running the Task Scheduler service that the user is connected to.</span></span><br/>          |



 

## <a name="examples"></a><span data-ttu-id="15cab-138">範例</span><span class="sxs-lookup"><span data-stu-id="15cab-138">Examples</span></span>

<span data-ttu-id="15cab-139">如需此腳本物件的詳細資訊和範例程式碼，請參閱[時間觸發程式範例 (腳本) ](time-trigger-example--scripting-.md)、[事件觸發程式範例 (腳本) ](https://www.bing.com/search?q=Event+Trigger+Example+(Scripting))、[每日觸發程式範例 (腳本](daily-trigger-example--scripting-.md)) 、[註冊觸發](registration-trigger-example--scripting-.md)程式範例 (腳本) 、[每週觸發](weekly-trigger-example--scripting-.md)程式範例 (腳本) 、[登入觸發](logon-trigger-example--scripting-.md)程式範例 (腳本) ，或顯示 (腳本[) 的工作](boot-trigger-example--scripting-.md)[名稱和狀態](displaying-task-names-and-state--scripting-.md)。</span><span class="sxs-lookup"><span data-stu-id="15cab-139">For more information and example code for this scripting object, see [Time Trigger Example (Scripting)](time-trigger-example--scripting-.md), [Event Trigger Example (Scripting)](https://www.bing.com/search?q=Event+Trigger+Example+(Scripting)), [Daily Trigger Example (Scripting)](daily-trigger-example--scripting-.md), [Registration Trigger Example (Scripting)](registration-trigger-example--scripting-.md), [Weekly Trigger Example (Scripting)](weekly-trigger-example--scripting-.md), [Logon Trigger Example (Scripting)](logon-trigger-example--scripting-.md), [Boot Trigger Example (Scripting)](boot-trigger-example--scripting-.md), or [Displaying Task Names and States (Scripting)](displaying-task-names-and-state--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="15cab-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="15cab-140">Requirements</span></span>



| <span data-ttu-id="15cab-141">需求</span><span class="sxs-lookup"><span data-stu-id="15cab-141">Requirement</span></span> | <span data-ttu-id="15cab-142">值</span><span class="sxs-lookup"><span data-stu-id="15cab-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="15cab-143">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="15cab-143">Minimum supported client</span></span><br/> | <span data-ttu-id="15cab-144">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="15cab-144">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="15cab-145">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="15cab-145">Minimum supported server</span></span><br/> | <span data-ttu-id="15cab-146">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="15cab-146">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="15cab-147">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="15cab-147">Type library</span></span><br/>             | <dl> <span data-ttu-id="15cab-148"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="15cab-148"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="15cab-149">DLL</span><span class="sxs-lookup"><span data-stu-id="15cab-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="15cab-150"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="15cab-150"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15cab-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="15cab-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15cab-152">工作排程器</span><span class="sxs-lookup"><span data-stu-id="15cab-152">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





