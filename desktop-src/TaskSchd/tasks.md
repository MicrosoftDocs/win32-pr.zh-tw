---
title: 工作
description: 工作是工作排程器服務執行的排程工作。
ms.assetid: 24c43834-5731-4b14-9409-7d7cf20b1a71
keywords:
- 工作工作排程器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efbb4ef41915ec70c98b59c9a7ba74c00f283ce6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106976324"
---
# <a name="tasks"></a><span data-ttu-id="49b4a-104">工作</span><span class="sxs-lookup"><span data-stu-id="49b4a-104">Tasks</span></span>

<span data-ttu-id="49b4a-105">工作是工作排程器服務執行的排程工作。</span><span class="sxs-lookup"><span data-stu-id="49b4a-105">A task is the scheduled work that the Task Scheduler service performs.</span></span> <span data-ttu-id="49b4a-106">工作是由不同的元件所組成，但是工作必須包含觸發程式，工作排程器使用此觸發程式來啟動工作，以及描述工作排程器將執行哪些工作的動作。</span><span class="sxs-lookup"><span data-stu-id="49b4a-106">A task is composed of different components, but a task must contain a trigger that the Task Scheduler uses to start the task and an action that describes what work the Task Scheduler will perform.</span></span>

<span data-ttu-id="49b4a-107">當工作建立時，它會儲存在工作資料夾中。</span><span class="sxs-lookup"><span data-stu-id="49b4a-107">When a task is created, it is stored in a task folder.</span></span> <span data-ttu-id="49b4a-108">您可以透過 [**ITaskFolder**](/windows/desktop/api/taskschd/nn-taskschd-itaskfolder) 介面 ([**TaskFolder**](taskfolder.md) 來存取工作資料夾，以編寫腳本) ，而且可以透過 [**IRegisteredTask**](/windows/desktop/api/taskschd/nn-taskschd-iregisteredtask) 介面存取工作資料夾， ([**RegisteredTask**](registeredtask.md) 在建立時使用腳本) 。</span><span class="sxs-lookup"><span data-stu-id="49b4a-108">Task folders can be accessed through the [**ITaskFolder**](/windows/desktop/api/taskschd/nn-taskschd-itaskfolder) interface ([**TaskFolder**](taskfolder.md) for scripting), and tasks can be accessed through the [**IRegisteredTask**](/windows/desktop/api/taskschd/nn-taskschd-iregisteredtask) interface ([**RegisteredTask**](registeredtask.md) for scripting) when they are created.</span></span> <span data-ttu-id="49b4a-109">您可以變更工作和工作資料夾 (Acl) 的存取控制清單，以授與或拒絕特定使用者和群組對工作或工作資料夾的存取權。</span><span class="sxs-lookup"><span data-stu-id="49b4a-109">You can change access control lists (ACLs) for tasks and task folders in order to grant or deny certain users and groups access to a task or task folder.</span></span> <span data-ttu-id="49b4a-110">這可以藉由使用 [**IRegisteredTask：： SetSecurityDescriptor**](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-setsecuritydescriptor) 方法、 [**ITaskFolder：： SetSecurityDescriptor**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-setsecuritydescriptor) 方法，或在使用 [**RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition) 或 [**RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) 方法註冊工作時指定安全描述項來完成。</span><span class="sxs-lookup"><span data-stu-id="49b4a-110">This can be done by using the [**IRegisteredTask::SetSecurityDescriptor**](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-setsecuritydescriptor) method, the [**ITaskFolder::SetSecurityDescriptor**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-setsecuritydescriptor) method, or by specifying a security descriptor when a task is registered by using the [**RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition) or [**RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) method.</span></span>

> [!Note]  
> <span data-ttu-id="49b4a-111">如果本機系統帳戶拒絕存取工作檔案或工作資料夾，工作排程器服務可能會產生非預期的結果。</span><span class="sxs-lookup"><span data-stu-id="49b4a-111">If the Local System account is denied access to a task file or task folder, then the Task Scheduler service can produce unexpected results.</span></span>

 

## <a name="components-of-a-task"></a><span data-ttu-id="49b4a-112">工作的元件</span><span class="sxs-lookup"><span data-stu-id="49b4a-112">Components of a Task</span></span>

<span data-ttu-id="49b4a-113">下圖顯示工作元件。</span><span class="sxs-lookup"><span data-stu-id="49b4a-113">The following illustration shows the task components.</span></span>

![工作元件](images/taskcomponents.png)

<span data-ttu-id="49b4a-115">下列清單包含每個工作元件的簡短描述：</span><span class="sxs-lookup"><span data-stu-id="49b4a-115">The following list contains a brief description of each task component:</span></span>

-   <span data-ttu-id="49b4a-116">觸發程式：工作排程器使用事件或以時間為基礎的觸發程式，以瞭解何時啟動工作。</span><span class="sxs-lookup"><span data-stu-id="49b4a-116">Triggers: Task Scheduler uses event or time-based triggers to know when to start a task.</span></span> <span data-ttu-id="49b4a-117">每項工作都可以指定一或多個觸發程式來啟動工作。</span><span class="sxs-lookup"><span data-stu-id="49b4a-117">Every task can specify one or more triggers to start the task.</span></span>

    <span data-ttu-id="49b4a-118">如需觸發程式的詳細資訊，請參閱工作 [觸發](task-triggers.md)程式。</span><span class="sxs-lookup"><span data-stu-id="49b4a-118">For more information about triggers, see [Task Triggers](task-triggers.md).</span></span>

-   <span data-ttu-id="49b4a-119">動作：這些是工作所執行的動作，也就是實際的工作。</span><span class="sxs-lookup"><span data-stu-id="49b4a-119">Actions: These are the actions, the actual work, that is performed by the task.</span></span> <span data-ttu-id="49b4a-120">每項工作都可以指定一或多個動作來完成其工作。</span><span class="sxs-lookup"><span data-stu-id="49b4a-120">Every task can specify one or more actions to complete its work.</span></span>

    <span data-ttu-id="49b4a-121">如需動作的詳細資訊，請參閱工作 [動作](task-actions.md)。</span><span class="sxs-lookup"><span data-stu-id="49b4a-121">For more information about actions, see [Task Actions](task-actions.md).</span></span>

-   <span data-ttu-id="49b4a-122">主體：主體會定義執行工作的安全性內容。</span><span class="sxs-lookup"><span data-stu-id="49b4a-122">Principals: Principals define the security context in which the task is run.</span></span> <span data-ttu-id="49b4a-123">例如，主體可能會定義可以執行工作的特定使用者或使用者群組。</span><span class="sxs-lookup"><span data-stu-id="49b4a-123">For example, a principal might define a specific user or user group that can run the task.</span></span>

    <span data-ttu-id="49b4a-124">如需主體的詳細資訊，請參閱工作 [的安全性](security-contexts-for-running-tasks.md)內容。</span><span class="sxs-lookup"><span data-stu-id="49b4a-124">For more information about principals, see [Security Contexts for Tasks](security-contexts-for-running-tasks.md).</span></span>

-   <span data-ttu-id="49b4a-125">設定：這些是工作排程器用來執行工作的設定，這些設定是針對工作本身以外的條件。</span><span class="sxs-lookup"><span data-stu-id="49b4a-125">Settings: These are the settings that the Task Scheduler uses to run the task with respect to conditions that are external to the task itself.</span></span> <span data-ttu-id="49b4a-126">例如，這些設定可以指定工作與其他工作相關的優先順序、是否可以執行工作的多個實例、在電腦處於閒置狀態時如何處理工作，以及其他條件。</span><span class="sxs-lookup"><span data-stu-id="49b4a-126">For example, these settings can specify the priority of the task with respect to other tasks, whether multiple instances of the task can be run, how the task is handled when the computer is in an idle condition, and other conditions.</span></span>

    <span data-ttu-id="49b4a-127">如需工作設定的詳細資訊，請參閱腳本) 的 [**ITaskSettings**](/windows/desktop/api/taskschd/nn-taskschd-itasksettings) ([**TaskSettings**](tasksettings.md) 。</span><span class="sxs-lookup"><span data-stu-id="49b4a-127">For more information about task settings, see [**ITaskSettings**](/windows/desktop/api/taskschd/nn-taskschd-itasksettings) ([**TaskSettings**](tasksettings.md) for scripting).</span></span>

    > [!Note]  
    > <span data-ttu-id="49b4a-128">根據預設，工作會在開始執行時停止72小時。</span><span class="sxs-lookup"><span data-stu-id="49b4a-128">By default, a task will be stopped 72 hours after it starts to run.</span></span> <span data-ttu-id="49b4a-129">您可以藉由變更 [**ExecutionTimeLimit**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_executiontimelimit) 設定來變更。</span><span class="sxs-lookup"><span data-stu-id="49b4a-129">You can change this by changing the [**ExecutionTimeLimit**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_executiontimelimit) setting.</span></span>

     

-   <span data-ttu-id="49b4a-130">註冊資訊：這是在註冊工作時所收集的系統管理資訊。</span><span class="sxs-lookup"><span data-stu-id="49b4a-130">Registration Information: This is administrative information that is gathered when the task is registered.</span></span> <span data-ttu-id="49b4a-131">例如，此資訊描述工作的作者、註冊工作的日期、工作的 XML 描述，以及其他資訊。</span><span class="sxs-lookup"><span data-stu-id="49b4a-131">For example, this information describes the author of the task, the date when the task was registered, an XML description of the task, and other information.</span></span>

    <span data-ttu-id="49b4a-132">如需工作註冊資訊的詳細資訊，請參閱工作 [註冊資訊](task-registration-information.md)。</span><span class="sxs-lookup"><span data-stu-id="49b4a-132">For more information about task registration information, see [Task Registration Information](task-registration-information.md).</span></span>

-   <span data-ttu-id="49b4a-133">Data：這是工作作者所提供之工作的其他檔。</span><span class="sxs-lookup"><span data-stu-id="49b4a-133">Data: This is additional documentation about the task that is supplied by the author of the task.</span></span> <span data-ttu-id="49b4a-134">例如，此資料可能包含使用者執行工作時可供使用者使用的 XML 說明。</span><span class="sxs-lookup"><span data-stu-id="49b4a-134">For example, this data may contain XML Help that can be used by users when they run the task.</span></span>

## <a name="task-apis"></a><span data-ttu-id="49b4a-135">工作 Api</span><span class="sxs-lookup"><span data-stu-id="49b4a-135">Task APIs</span></span>

<span data-ttu-id="49b4a-136">工作排程器2.0 提供兩組 Api：工作排程器2.0 的一組腳本物件和介面。</span><span class="sxs-lookup"><span data-stu-id="49b4a-136">Task Scheduler 2.0 provides two sets of APIs: a set of scripting objects and interfaces for Task Scheduler 2.0.</span></span> <span data-ttu-id="49b4a-137">如需詳細資訊，請參閱 [工作排程器參考](task-scheduler-reference.md)。</span><span class="sxs-lookup"><span data-stu-id="49b4a-137">For more information, see [Task Scheduler Reference](task-scheduler-reference.md).</span></span>

<span data-ttu-id="49b4a-138">[](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_compatibility) \_ \_ 如果工作必須從 Windows XP、Windows Server 2003 或 windows 2000 電腦存取或修改，則透過 [相容性] 屬性所設定的工作相容性只應設定為 [工作相容性 V1]。</span><span class="sxs-lookup"><span data-stu-id="49b4a-138">Task compatibility, which is set through the [**Compatibility**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_compatibility) property, should only be set to TASK\_COMPATIBILITY\_V1 if a task must be accessed or modified from a Windows XP, Windows Server 2003, or Windows 2000 computer.</span></span> <span data-ttu-id="49b4a-139">否則，建議您使用工作排程器2.0 相容性，因為它有更多功能。</span><span class="sxs-lookup"><span data-stu-id="49b4a-139">Otherwise, it is recommended that you use Task Scheduler 2.0 compatibility because it has more features.</span></span>

<span data-ttu-id="49b4a-140">從工作排程器2.0 開始，腳本) 的 [**ITaskService**](/windows/desktop/api/taskschd/nn-taskschd-itaskservice) 介面 ([**TaskService**](taskservice.md) ，是用來在指定的資料夾中建立工作的起點。</span><span class="sxs-lookup"><span data-stu-id="49b4a-140">Starting with Task Scheduler 2.0, the [**ITaskService**](/windows/desktop/api/taskschd/nn-taskschd-itaskservice) interface ([**TaskService**](taskservice.md) for scripting) is used as a starting point to create tasks in specified folders.</span></span> <span data-ttu-id="49b4a-141">腳本) 的 [**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) 介面 ([**TaskDefinition**](taskdefinition.md) 用來保存工作的所有元件，例如設定、動作和觸發程式。</span><span class="sxs-lookup"><span data-stu-id="49b4a-141">The [**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) interface ([**TaskDefinition**](taskdefinition.md) for scripting) is used to hold all the components of a task, such as the settings, actions, and triggers.</span></span> <span data-ttu-id="49b4a-142">[**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger)、 [**IAction**](/windows/desktop/api/taskschd/nn-taskschd-iaction)和 [**ITaskSettings**](/windows/desktop/api/taskschd/nn-taskschd-itasksettings) api 提供的屬性，可用來定義工作的其他元件。</span><span class="sxs-lookup"><span data-stu-id="49b4a-142">The [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger), [**IAction**](/windows/desktop/api/taskschd/nn-taskschd-iaction), and [**ITaskSettings**](/windows/desktop/api/taskschd/nn-taskschd-itasksettings) APIs provide properties that are then used to define the other components of the task.</span></span> <span data-ttu-id="49b4a-143">工作排程器1.0 提供僅為了回溯相容性所支援的 [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) 介面。</span><span class="sxs-lookup"><span data-stu-id="49b4a-143">Task Scheduler 1.0 provides the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface, which is supported only for backward compatibility.</span></span>

<span data-ttu-id="49b4a-144">針對腳本，工作排程器介面會對應到具有類似名稱、屬性和方法的腳本物件。</span><span class="sxs-lookup"><span data-stu-id="49b4a-144">For scripting, the Task Scheduler interfaces map to scripting objects that have the similar names, properties, and methods.</span></span> <span data-ttu-id="49b4a-145">例如， [**TaskService**](taskservice.md) 腳本物件具有與 [**ITaskService**](/windows/desktop/api/taskschd/nn-taskschd-itaskservice) 介面相同的屬性和方法。</span><span class="sxs-lookup"><span data-stu-id="49b4a-145">For example, the [**TaskService**](taskservice.md) scripting object has the same properties and methods as the [**ITaskService**](/windows/desktop/api/taskschd/nn-taskschd-itaskservice) interface.</span></span>

<span data-ttu-id="49b4a-146">如需有關如何使用工作排程器介面、腳本物件和 XML 的詳細資訊和範例，請參閱 [使用工作排程器](using-the-task-scheduler.md)。</span><span class="sxs-lookup"><span data-stu-id="49b4a-146">For more information and examples about how to use the Task Scheduler interfaces, scripting objects, and XML, see [Using the Task Scheduler](using-the-task-scheduler.md).</span></span>

### <a name="task-scheduler-10-tasks"></a><span data-ttu-id="49b4a-147">工作排程器1.0 工作</span><span class="sxs-lookup"><span data-stu-id="49b4a-147">Task Scheduler 1.0 Tasks</span></span>

<span data-ttu-id="49b4a-148">工作排程器1.0 工作是工作排程器可執行檔任何應用程式或檔案類型。</span><span class="sxs-lookup"><span data-stu-id="49b4a-148">A Task Scheduler 1.0 task is any application or file type that the Task Scheduler can execute.</span></span> <span data-ttu-id="49b4a-149">這些可能包括工作執行所在作業系統所支援的下列任何 () ： Win32 應用程式、Win16 應用程式、OS/2 應用程式、MS-DOS 應用程式、批次檔 (\* .bat) 、命令檔 (\* .cmd) 或任何正確註冊的檔案類型。</span><span class="sxs-lookup"><span data-stu-id="49b4a-149">These may include any of the following (as supported by the operating system on which the task will execute): Win32 applications, Win16 applications, OS/2 applications, MS-DOS applications, batch files (\*.bat), command files (\*.cmd), or any properly registered file type.</span></span>

<span data-ttu-id="49b4a-150">描述工作的資料會保存在儲存在 [排程工作] 資料夾中的工作檔案。</span><span class="sxs-lookup"><span data-stu-id="49b4a-150">Data that describes a task is kept in a task file that is stored in the Scheduled Tasks folder.</span></span> <span data-ttu-id="49b4a-151">如需詳細資訊，請參閱排程的工作 [*資料夾*](s.md)。</span><span class="sxs-lookup"><span data-stu-id="49b4a-151">For more information, see [*Scheduled Tasks folder*](s.md).</span></span> <span data-ttu-id="49b4a-152">這些工作檔的名稱包括工作的名稱，後面接著一個. 作業副檔名。</span><span class="sxs-lookup"><span data-stu-id="49b4a-152">The name of these task files include the name of the task, followed by a .job file name extension.</span></span>

<span data-ttu-id="49b4a-153">如需新增工作排程器1.0 工作的詳細資訊，請參閱 [加入工作專案](adding-work-items.md)。</span><span class="sxs-lookup"><span data-stu-id="49b4a-153">For more information about adding Task Scheduler 1.0 tasks, see [Adding Work Items](adding-work-items.md).</span></span>

<span data-ttu-id="49b4a-154">如需列舉工作排程器1.0 工作的詳細資訊，請參閱列舉工作（ [task](enumerating-tasks.md)）。</span><span class="sxs-lookup"><span data-stu-id="49b4a-154">For more information about enumerating through Task Scheduler 1.0 tasks, see [Enumerating Tasks](enumerating-tasks.md).</span></span>

<span data-ttu-id="49b4a-155">若為 Windows Server 2003、Windows XP 或 Windows 2000 電腦，可在 Windows Vista 電腦上建立、監視或控制工作，則應該在 Windows Vista 電腦上完成下列操作，而且呼叫 [**ITaskScheduler：： SetTargetComputer**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-settargetcomputer) 方法的使用者必須是遠端 Windows vista 電腦上的 Administrators 群組成員。</span><span class="sxs-lookup"><span data-stu-id="49b4a-155">For a Windows Server 2003, Windows XP, or Windows 2000 computer to create, monitor, or control tasks on a Windows Vista computer, the following operations should be completed on the Windows Vista computer, and the user who is calling the [**ITaskScheduler::SetTargetComputer**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-settargetcomputer) method must be a member of the Administrators group on the remote Windows Vista computer.</span></span>

<span data-ttu-id="49b4a-156">**若要在 Windows 防火牆中啟用「共用檔案和印表機」例外狀況**</span><span class="sxs-lookup"><span data-stu-id="49b4a-156">**To enable the "Share File and Printers" exception in Windows Firewall**</span></span>

1.  <span data-ttu-id="49b4a-157">按一下 [開始]，然後按一下 [控制台]。</span><span class="sxs-lookup"><span data-stu-id="49b4a-157">Click **Start**, and then click **Control Panel**.</span></span>
2.  <span data-ttu-id="49b4a-158">在 **主控台** 中，按一下 [ **傳統視圖** ]，然後按兩下 [ **Windows 防火牆** ] 圖示。</span><span class="sxs-lookup"><span data-stu-id="49b4a-158">In **Control Panel**, click **Classic View** and then double-click the **Windows Firewall** icon.</span></span>
3.  <span data-ttu-id="49b4a-159">在 [ **Windows 防火牆** ] 視窗中，按一下 [ **例外** 狀況] 索引標籤，然後選取 [檔案 **和印表機共用例外** ] 核取方塊。</span><span class="sxs-lookup"><span data-stu-id="49b4a-159">In the **Windows Firewall** window, click the **Exceptions** tab and select **File and Printer Sharing exception** check box.</span></span>

<span data-ttu-id="49b4a-160">**啟用「遠端登入」服務**</span><span class="sxs-lookup"><span data-stu-id="49b4a-160">**To enable the "Remote Registry" service**</span></span>

-   <span data-ttu-id="49b4a-161">開啟 [命令提示字元] 視窗，然後輸入下列命令： **net start "Remote Registry"**。</span><span class="sxs-lookup"><span data-stu-id="49b4a-161">Open a Command Prompt window and enter the following command: **net start "Remote Registry"**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="49b4a-162">相關主題</span><span class="sxs-lookup"><span data-stu-id="49b4a-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="49b4a-163">關於工作排程器</span><span class="sxs-lookup"><span data-stu-id="49b4a-163">About the Task Scheduler</span></span>](about-the-task-scheduler.md)
</dt> <dt>

[<span data-ttu-id="49b4a-164">工作觸發程式</span><span class="sxs-lookup"><span data-stu-id="49b4a-164">Task Triggers</span></span>](task-triggers.md)
</dt> <dt>

[<span data-ttu-id="49b4a-165">工作動作</span><span class="sxs-lookup"><span data-stu-id="49b4a-165">Task Actions</span></span>](task-actions.md)
</dt> <dt>

[<span data-ttu-id="49b4a-166">**ITaskDefinition**</span><span class="sxs-lookup"><span data-stu-id="49b4a-166">**ITaskDefinition**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition)
</dt> <dt>

[<span data-ttu-id="49b4a-167">**TaskDefinition**</span><span class="sxs-lookup"><span data-stu-id="49b4a-167">**TaskDefinition**</span></span>](taskdefinition.md)
</dt> <dt>

[<span data-ttu-id="49b4a-168">**ITaskService**</span><span class="sxs-lookup"><span data-stu-id="49b4a-168">**ITaskService**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-itaskservice)
</dt> <dt>

[<span data-ttu-id="49b4a-169">**TaskService**</span><span class="sxs-lookup"><span data-stu-id="49b4a-169">**TaskService**</span></span>](taskservice.md)
</dt> </dl>

 

 




