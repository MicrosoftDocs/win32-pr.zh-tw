---
title: 工作排程器的新功能
description: 不同工作排程器版本所引進的新功能清單。
ms.assetid: 43fbbbd2-6e97-4ba5-9474-23c5e2b33612
keywords:
- 工作排程器工作排程器，新功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5245ab4e681af937924cfbd217095009d80d6a11
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106991655"
---
# <a name="whats-new-in-task-scheduler"></a><span data-ttu-id="b4435-104">工作排程器的新功能</span><span class="sxs-lookup"><span data-stu-id="b4435-104">What's New in Task Scheduler</span></span>

<span data-ttu-id="b4435-105">下列變更摘要說明不同工作排程器版本的新功能。</span><span class="sxs-lookup"><span data-stu-id="b4435-105">The following changes summarize what is new in different versions of Task Scheduler.</span></span>

## <a name="windows-10-and-windows-server-2016"></a><span data-ttu-id="b4435-106">Windows 10 (和 Windows Server 2016) </span><span class="sxs-lookup"><span data-stu-id="b4435-106">Windows 10 (and Windows Server 2016)</span></span>

<span data-ttu-id="b4435-107">Windows 10 引進了下列工作排程器變更。</span><span class="sxs-lookup"><span data-stu-id="b4435-107">The following Task Scheduler changes are introduced in Windows 10.</span></span>

-   <span data-ttu-id="b4435-108">當省電模式開啟時，只有當工作為時，才會觸發 Windows 工作排程器工作：</span><span class="sxs-lookup"><span data-stu-id="b4435-108">When battery saver is on, Windows Task Scheduler tasks are triggered only if the task is:</span></span>

    -   <span data-ttu-id="b4435-109">未設定為 **只在電腦閒置時才啟動工作** ... (工作不使用 [**IdleSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_idlesettings)) </span><span class="sxs-lookup"><span data-stu-id="b4435-109">Not set to **Start the task only if the computer is idle...** (task doesn't use [**IdleSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_idlesettings))</span></span>
    -   <span data-ttu-id="b4435-110">未設定為在自動維護期間執行 (工作不會使用 [**MaintenanceSettings**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_maintenancesettings)) </span><span class="sxs-lookup"><span data-stu-id="b4435-110">Not set to run during automatic maintenance (task doesn't use [**MaintenanceSettings**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_maintenancesettings))</span></span>
    -   <span data-ttu-id="b4435-111">設定為 **只有在使用者登入時才會執行** (工作 [**LogonType**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_logontype) 是工作 **登入 \_ \_ 互動式 \_ 權杖** 或工作 **登入 \_ \_ 群組**) </span><span class="sxs-lookup"><span data-stu-id="b4435-111">Is set to **Run only when user is logged on** (task [**LogonType**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_logontype) is **TASK\_LOGON\_INTERACTIVE\_TOKEN** or **TASK\_LOGON\_GROUP**)</span></span>

    <span data-ttu-id="b4435-112">所有其他觸發程式都會延遲到省電模式關閉為止。</span><span class="sxs-lookup"><span data-stu-id="b4435-112">All other triggers are delayed until battery saver is off.</span></span> <span data-ttu-id="b4435-113">如需有關在應用程式中存取省電模式狀態的詳細資訊，請參閱 [**系統 \_ 電源 \_ 狀態**](/windows/desktop/api/winbase/ns-winbase-system_power_status)。</span><span class="sxs-lookup"><span data-stu-id="b4435-113">For more information about accessing battery saver status in your application, see [**SYSTEM\_POWER\_STATUS**](/windows/desktop/api/winbase/ns-winbase-system_power_status).</span></span> <span data-ttu-id="b4435-114">如需有關省電模式的一般資訊，請參閱 [硬體元件指導方針中的省電模式 () ](/windows-hardware/design/component-guidelines/battery-saver)。</span><span class="sxs-lookup"><span data-stu-id="b4435-114">For general information about battery saver, see [battery saver (in the hardware component guidelines)](/windows-hardware/design/component-guidelines/battery-saver).</span></span>

-   <span data-ttu-id="b4435-115">基於安全性理由，非系統管理員使用者無法查看或管理另一位使用者所建立的 Windows 工作排程器工作。</span><span class="sxs-lookup"><span data-stu-id="b4435-115">For security reasons, a non-administrator user cannot view nor manage a Windows Task Scheduler task that was created by another user.</span></span>

## <a name="windows-8"></a><span data-ttu-id="b4435-116">Windows 8</span><span class="sxs-lookup"><span data-stu-id="b4435-116">Windows 8</span></span>

<span data-ttu-id="b4435-117">Windows 8 引進下列工作排程器2.0 變更：</span><span class="sxs-lookup"><span data-stu-id="b4435-117">The following Task Scheduler 2.0 changes are introduced in Windows 8:</span></span>

-   <span data-ttu-id="b4435-118">Powershell 支援：使用者可以使用 ScheduledTasks powershell 模組來管理 (建立、刪除、修改、明確啟動、停止等 ) Windows 工作排程器工作。</span><span class="sxs-lookup"><span data-stu-id="b4435-118">Powershell support: users can manage (create, delete, modify, explicitly start, stop etc.) Windows Task Scheduler tasks using the ScheduledTasks powershell module.</span></span>
-   <span data-ttu-id="b4435-119">受控密碼：系統管理員可以使用 Active Directory 管理的密碼帳戶做為工作主體。</span><span class="sxs-lookup"><span data-stu-id="b4435-119">Managed passwords: administrators can use the Active Directory managed password accounts as task principals.</span></span> <span data-ttu-id="b4435-120">這些工作不再需要強制執行的密碼重設原則。</span><span class="sxs-lookup"><span data-stu-id="b4435-120">These tasks no longer require an enforced password reset policy.</span></span>
-   <span data-ttu-id="b4435-121">API 變更：引進兩個具有 [**ITaskSettings3**](/windows/desktop/api/taskschd/nn-taskschd-itasksettings3) 介面的新工作設定。</span><span class="sxs-lookup"><span data-stu-id="b4435-121">API changes: Introduced two new task settings with the [**ITaskSettings3**](/windows/desktop/api/taskschd/nn-taskschd-itasksettings3) interface.</span></span>
    -   <span data-ttu-id="b4435-122">[**MaintenanceSettings**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_maintenancesettings)：使用這些設定的工作會被視為一種新的排程工作，這些工作會根據指定的週期和期限，在 OS 自動維護期間叫用。</span><span class="sxs-lookup"><span data-stu-id="b4435-122">[**MaintenanceSettings**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_maintenancesettings): tasks using these settings are treated as a new type of scheduled tasks that are invoked during OS automatic maintenance time, according to the specified periodicity and deadline.</span></span>
    -   <span data-ttu-id="b4435-123">[**Volatile**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_volatile)：設定為 volatile 的工作一律會在 OS 開機時停用，而且必須在必要時明確重新啟用。</span><span class="sxs-lookup"><span data-stu-id="b4435-123">[**Volatile**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_volatile): tasks that are set to be volatile are always disabled on an OS boot and must be explicitly re-enabled back when required.</span></span> <span data-ttu-id="b4435-124">「容錯移轉叢集」會利用 Volatile 工作，以確保一次只在一個叢集上排程一個工作實例。</span><span class="sxs-lookup"><span data-stu-id="b4435-124">Volatile tasks are utilized by the failover clusters to ensure only one task instance is scheduled on a cluster at a time.</span></span>
-   <span data-ttu-id="b4435-125">整合排程引擎現在支援下列功能：</span><span class="sxs-lookup"><span data-stu-id="b4435-125">The unified scheduling engine now supports the following features:</span></span>
    -   <span data-ttu-id="b4435-126">S4U 登入類型（透過 [**LogonType**](taskschedulerschema-logontype-principaltype-element.md) 元素）。</span><span class="sxs-lookup"><span data-stu-id="b4435-126">S4U Logon type, through the [**LogonType**](taskschedulerschema-logontype-principaltype-element.md) element.</span></span>
    -   <span data-ttu-id="b4435-127">事件觸發程式的 XPath 查詢值（透過 [**ValueQueries**](taskschedulerschema-valuequeries-eventtriggertype-element.md) 元素）。</span><span class="sxs-lookup"><span data-stu-id="b4435-127">XPath query values for event triggers, through the [**ValueQueries**](taskschedulerschema-valuequeries-eventtriggertype-element.md) element.</span></span>
    -   <span data-ttu-id="b4435-128">不允許透過 [**AllowHardTerminate**](taskschedulerschema-allowhardterminate-settingstype-element.md) 元素進行工作硬終止。</span><span class="sxs-lookup"><span data-stu-id="b4435-128">Do not allow task hard terminate, through the [**AllowHardTerminate**](taskschedulerschema-allowhardterminate-settingstype-element.md) element.</span></span>
-   <span data-ttu-id="b4435-129">此版本中已淘汰的功能</span><span class="sxs-lookup"><span data-stu-id="b4435-129">Features deprecated in this release</span></span>
    -   <span data-ttu-id="b4435-130">Action： [**sendEmail**](taskschedulerschema-sendemail-actiongroup-element.md) (您可以使用 [**IExecAction**](/windows/desktop/api/taskschd/nn-taskschd-iexecaction)搭配 [Windows PowerShell](https://technet.microsoft.com/library/bb978526.aspx)的 [傳送 send-mailmessage](/powershell/module/microsoft.powershell.utility/send-mailmessage?view=powershell-7&preserve-view=true) Cmdlet 作為因應措施) 。</span><span class="sxs-lookup"><span data-stu-id="b4435-130">Action: [**sendEmail**](taskschedulerschema-sendemail-actiongroup-element.md) (you can use [**IExecAction**](/windows/desktop/api/taskschd/nn-taskschd-iexecaction) with the [Windows PowerShell](https://technet.microsoft.com/library/bb978526.aspx)[Send-MailMessage](/powershell/module/microsoft.powershell.utility/send-mailmessage?view=powershell-7&preserve-view=true) cmdlet as a workaround).</span></span>
    -   <span data-ttu-id="b4435-131">Action： [**showMessage**](taskschedulerschema-showmessage-actiongroup-element.md)。</span><span class="sxs-lookup"><span data-stu-id="b4435-131">Action: [**showMessage**](taskschedulerschema-showmessage-actiongroup-element.md).</span></span>
    -   <span data-ttu-id="b4435-132">AT.exe cmdline 公用程式</span><span class="sxs-lookup"><span data-stu-id="b4435-132">AT.exe cmdline utility</span></span>

## <a name="windows-7"></a><span data-ttu-id="b4435-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b4435-133">Windows 7</span></span>

<span data-ttu-id="b4435-134">Windows 7 中引進了下列工作排程器2.0 變更：</span><span class="sxs-lookup"><span data-stu-id="b4435-134">The following Task Scheduler 2.0 changes are introduced in Windows 7:</span></span>

-   <span data-ttu-id="b4435-135">使用基礎作業系統所提供的統一排程引擎。</span><span class="sxs-lookup"><span data-stu-id="b4435-135">Using the unified scheduling engine provided by the underlying operating system.</span></span>
-   <span data-ttu-id="b4435-136">能夠拒絕遠端應用程式中的啟動工作，這些工作是在遠端應用程式的本機 (滑軌) 會話</span><span class="sxs-lookup"><span data-stu-id="b4435-136">Ability to reject starting tasks in Remote Applications Integrated Locally (RAIL) sessions.</span></span>
-   <span data-ttu-id="b4435-137">工作安全性強化 (針對以「網路服務」或「本機服務」執行的工作，只) ：</span><span class="sxs-lookup"><span data-stu-id="b4435-137">Task security hardening (for tasks running as "NETWORK SERVICE" or "LOCAL SERVICE" only):</span></span>

    -   <span data-ttu-id="b4435-138">能夠將進程權杖安全識別碼指派 (SID) 類型 (例如，不受限制或無) 至工作。</span><span class="sxs-lookup"><span data-stu-id="b4435-138">Ability to assign a process token security identifier (SID) type (for example, unrestricted or none) to a task.</span></span>
    -   <span data-ttu-id="b4435-139">允許工作開發人員要求其工作所需的一組完整許可權。</span><span class="sxs-lookup"><span data-stu-id="b4435-139">Allow task developers to request the exact set of privileges that their task requires.</span></span>

-   <span data-ttu-id="b4435-140">API 變更：</span><span class="sxs-lookup"><span data-stu-id="b4435-140">API changes:</span></span>

    -   <span data-ttu-id="b4435-141">工作安全性強化支援：新的 IPrincipal2 介面引進了新的任務安全性強化功能。</span><span class="sxs-lookup"><span data-stu-id="b4435-141">Task security hardening support: new task security hardening feature is introduced with new IPrincipal2 interface.</span></span>
    -   <span data-ttu-id="b4435-142">引進了新的 ITaskSettings2 介面的兩個新工作設定。</span><span class="sxs-lookup"><span data-stu-id="b4435-142">Introduced two new task settings with the new ITaskSettings2 interface.</span></span>

        -   <span data-ttu-id="b4435-143">DisallowStartOnRemoteAppSession：如果是在 [遠端應用程式中，在遠端應用程式中進行 (整合，) ](/openspecs/windows_protocols/MS-WINPROTLP/df36f95e-6a6b-48d6-a3ae-35a17674f546) 會話，則新的 DisallowStartOnRemoteAppSession 設定可能會拒絕工作啟動。</span><span class="sxs-lookup"><span data-stu-id="b4435-143">DisallowStartOnRemoteAppSession: The new DisallowStartOnRemoteAppSession setting can reject a task start if triggered in [Remote Applications Integrated Locally (RAIL)](/openspecs/windows_protocols/MS-WINPROTLP/df36f95e-6a6b-48d6-a3ae-35a17674f546) sessions.</span></span>
        -   <span data-ttu-id="b4435-144">UseUnifiedSchedulingEngine：使用 UseUnifiedSchedulingEngine 設定可為 Windows 工作和服務提供一致的行為，因為它是以統一的方式，由一般全系統排程引擎進行管理。</span><span class="sxs-lookup"><span data-stu-id="b4435-144">UseUnifiedSchedulingEngine: Using the UseUnifiedSchedulingEngine setting provides a cohesive behavior for Windows Tasks and Services because it is being managed in a uniform manner by a common system-wide scheduling engine.</span></span> <span data-ttu-id="b4435-145">雖然建議使用整合引擎，但不支援某些工作排程器功能。</span><span class="sxs-lookup"><span data-stu-id="b4435-145">Although using a unified engine is recommended, it does not support some of the Task Scheduler features.</span></span> <span data-ttu-id="b4435-146">如果屬性的組合不允許在統一引擎下執行工作，則會拒絕這類的註冊。</span><span class="sxs-lookup"><span data-stu-id="b4435-146">If the combination of properties will not allow running of the task under a unified engine, the registration of such will be rejected.</span></span>
        -   <span data-ttu-id="b4435-147">整合排程引擎不支援的工作功能包括：</span><span class="sxs-lookup"><span data-stu-id="b4435-147">The task features that are not supported by the unified scheduling engine include:</span></span>

            -   <span data-ttu-id="b4435-148">登入類型：</span><span class="sxs-lookup"><span data-stu-id="b4435-148">Logon types:</span></span>

                -   [<span data-ttu-id="b4435-149">工作 \_ 登入 \_ 互動式 \_ 權杖 \_ 或 \_ 密碼</span><span class="sxs-lookup"><span data-stu-id="b4435-149">TASK\_LOGON\_INTERACTIVE\_TOKEN\_OR\_PASSWORD</span></span>](./taskschedulerschema-logontype-principaltype-element.md)

            -   <span data-ttu-id="b4435-150">多個實例原則：</span><span class="sxs-lookup"><span data-stu-id="b4435-150">Multiple instance policy:</span></span>

                -   [<span data-ttu-id="b4435-151">**工作 \_ 實例 \_ 停止 \_ 現有的**</span><span class="sxs-lookup"><span data-stu-id="b4435-151">**TASK\_INSTANCES\_STOP\_EXISTING**</span></span>](taskschedulerschema-multipleinstancespolicy-settingstype-element.md)

            -   <span data-ttu-id="b4435-152">動作：</span><span class="sxs-lookup"><span data-stu-id="b4435-152">Actions:</span></span>

                -   [<span data-ttu-id="b4435-153">傳送電子郵件</span><span class="sxs-lookup"><span data-stu-id="b4435-153">Send email</span></span>](./taskschedulerschema-sendemail-actiongroup-element.md)
                -   [<span data-ttu-id="b4435-154">顯示訊息</span><span class="sxs-lookup"><span data-stu-id="b4435-154">Display message</span></span>](./taskschedulerschema-showmessage-actiongroup-element.md)

            -   <span data-ttu-id="b4435-155">設定：</span><span class="sxs-lookup"><span data-stu-id="b4435-155">Settings:</span></span>

                -   [<span data-ttu-id="b4435-156">工作網路設定</span><span class="sxs-lookup"><span data-stu-id="b4435-156">Task network settings</span></span>](./taskschedulerschema-networksettings-settingstype-element.md)
                -   [<span data-ttu-id="b4435-157">不允許工作硬終止</span><span class="sxs-lookup"><span data-stu-id="b4435-157">Do not allow task hard terminate</span></span>](./taskschedulerschema-allowhardterminate-settingstype-element.md)

            -   <span data-ttu-id="b4435-158">觸發程序：</span><span class="sxs-lookup"><span data-stu-id="b4435-158">Triggers:</span></span>

                -   [<span data-ttu-id="b4435-159">觸發程式執行時間限制</span><span class="sxs-lookup"><span data-stu-id="b4435-159">Trigger execution time limit</span></span>](./taskschedulerschema-executiontimelimit-triggerbasetype-element.md)
                -   [<span data-ttu-id="b4435-160">行事曆觸發程式的重複模式</span><span class="sxs-lookup"><span data-stu-id="b4435-160">Repetition patterns for calendar triggers</span></span>]( ./taskschedulerschema-repetition-triggerbasetype-element.md)
                -   [<span data-ttu-id="b4435-161">事件觸發程式的 XPath 查詢值</span><span class="sxs-lookup"><span data-stu-id="b4435-161">XPath query values for event triggers</span></span>]( ./taskschedulerschema-valuequeries-eventtriggertype-element.md)
                -   <span data-ttu-id="b4435-162">[每月](./taskschedulerschema-schedulebymonth-calendartriggertype-element.md) 和 [每月星期幾](./taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) 觸發程式類型</span><span class="sxs-lookup"><span data-stu-id="b4435-162">[Monthly](./taskschedulerschema-schedulebymonth-calendartriggertype-element.md) and [Monthly day-of-week](./taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) trigger types</span></span>

## <a name="windows-vista"></a><span data-ttu-id="b4435-163">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b4435-163">Windows Vista</span></span>

<span data-ttu-id="b4435-164">工作排程器 2.0 API 應該用於開發在 Windows Vista 上使用工作排程器服務的應用程式。</span><span class="sxs-lookup"><span data-stu-id="b4435-164">The Task Scheduler 2.0 API should be used in developing applications that use the Task Scheduler service on Windows Vista.</span></span> <span data-ttu-id="b4435-165">如需詳細資訊，請參閱 [工作排程器參考](task-scheduler-reference.md) 和 [使用工作排程器](using-the-task-scheduler.md)。</span><span class="sxs-lookup"><span data-stu-id="b4435-165">For more information, see [Task Scheduler Reference](task-scheduler-reference.md) and [Using the Task Scheduler](using-the-task-scheduler.md).</span></span>

## <a name="windows-2000-windows-xp-and-windows-server-2003"></a><span data-ttu-id="b4435-166">Windows 2000、Windows XP 及 Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b4435-166">Windows 2000, Windows XP, and Windows Server 2003</span></span>

<span data-ttu-id="b4435-167">無法使用工作排程器 2.0 API。</span><span class="sxs-lookup"><span data-stu-id="b4435-167">The Task Scheduler 2.0 API is not available.</span></span> <span data-ttu-id="b4435-168">使用工作排程器1.0。</span><span class="sxs-lookup"><span data-stu-id="b4435-168">Use Task Scheduler 1.0.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b4435-169">相關主題</span><span class="sxs-lookup"><span data-stu-id="b4435-169">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b4435-170">工作排程器</span><span class="sxs-lookup"><span data-stu-id="b4435-170">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="b4435-171">關於工作排程器</span><span class="sxs-lookup"><span data-stu-id="b4435-171">About The Task Scheduler</span></span>](about-the-task-scheduler.md)
</dt> </dl>

 

 
