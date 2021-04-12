---
title: " (taskType) 元素設定"
description: 指定工作排程器用來執行工作的設定。
ms.assetid: 72d2929a-0dd2-44cd-be7b-72eca23a5e14
keywords:
- Settings 元素工作排程器
topic_type:
- apiref
api_name:
- Settings
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9133d536aef692a5f9928e10963dff8c454f25fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384357"
---
# <a name="settings-tasktype-element"></a><span data-ttu-id="ebd46-104"> (taskType) 元素設定</span><span class="sxs-lookup"><span data-stu-id="ebd46-104">Settings (taskType) Element</span></span>

<span data-ttu-id="ebd46-105">指定工作排程器用來執行工作的設定。</span><span class="sxs-lookup"><span data-stu-id="ebd46-105">Specifies the settings that the Task Scheduler uses to perform the task.</span></span>

``` syntax
<xs:element name="Settings"
    type="settingsType"
    minOccurs="0"
 />
```

<span data-ttu-id="ebd46-106">**Settings** 元素是由 [**taskType**](taskschedulerschema-tasktype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="ebd46-106">The **Settings** element is defined by the [**taskType**](taskschedulerschema-tasktype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="ebd46-107">父元素</span><span class="sxs-lookup"><span data-stu-id="ebd46-107">Parent element</span></span>



| <span data-ttu-id="ebd46-108">元素</span><span class="sxs-lookup"><span data-stu-id="ebd46-108">Element</span></span>                                          | <span data-ttu-id="ebd46-109">衍生自</span><span class="sxs-lookup"><span data-stu-id="ebd46-109">Derived from</span></span>                                                 | <span data-ttu-id="ebd46-110">Description</span><span class="sxs-lookup"><span data-stu-id="ebd46-110">Description</span></span>                                                                    |
|--------------------------------------------------|--------------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="ebd46-111">**Task**</span><span class="sxs-lookup"><span data-stu-id="ebd46-111">**Task**</span></span>](taskschedulerschema-task-element.md) | [<span data-ttu-id="ebd46-112">**taskType**</span><span class="sxs-lookup"><span data-stu-id="ebd46-112">**taskType**</span></span>](taskschedulerschema-tasktype-complextype.md) | <span data-ttu-id="ebd46-113">指定工作排程器服務所執行的工作。</span><span class="sxs-lookup"><span data-stu-id="ebd46-113">Specifies the task that is performed by the Task Scheduler service.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="ebd46-114">子元素</span><span class="sxs-lookup"><span data-stu-id="ebd46-114">Child elements</span></span>



| <span data-ttu-id="ebd46-115">元素</span><span class="sxs-lookup"><span data-stu-id="ebd46-115">Element</span></span>                                                                                                          | <span data-ttu-id="ebd46-116">類型</span><span class="sxs-lookup"><span data-stu-id="ebd46-116">Type</span></span>                                                                                              | <span data-ttu-id="ebd46-117">Description</span><span class="sxs-lookup"><span data-stu-id="ebd46-117">Description</span></span>                                                                                                          |
|------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ebd46-118">**AllowHardTerminate**</span><span class="sxs-lookup"><span data-stu-id="ebd46-118">**AllowHardTerminate**</span></span>](taskschedulerschema-allowhardterminate-settingstype-element.md)                        | <span data-ttu-id="ebd46-119">boolean</span><span class="sxs-lookup"><span data-stu-id="ebd46-119">boolean</span></span>                                                                                           | <span data-ttu-id="ebd46-120">指定可以使用 TerminateProcess 終止工作。</span><span class="sxs-lookup"><span data-stu-id="ebd46-120">Specifies that the task may be terminated using TerminateProcess.</span></span><br/>                                         |
| [<span data-ttu-id="ebd46-121">**AllowStartOnDemand**</span><span class="sxs-lookup"><span data-stu-id="ebd46-121">**AllowStartOnDemand**</span></span>](taskschedulerschema-allowstartondemand-settingstype-element.md)                        | <span data-ttu-id="ebd46-122">boolean</span><span class="sxs-lookup"><span data-stu-id="ebd46-122">boolean</span></span>                                                                                           | <span data-ttu-id="ebd46-123">指定可使用 [執行] 命令或內容功能表來啟動工作。</span><span class="sxs-lookup"><span data-stu-id="ebd46-123">Specifies that the task can be started using either the Run command or the Context menu.</span></span><br/>                  |
| [<span data-ttu-id="ebd46-124">**DeleteExpiredTaskAfter**</span><span class="sxs-lookup"><span data-stu-id="ebd46-124">**DeleteExpiredTaskAfter**</span></span>](taskschedulerschema-deleteexpiredtaskafter-settingstype-element.md)                | <span data-ttu-id="ebd46-125">duration</span><span class="sxs-lookup"><span data-stu-id="ebd46-125">duration</span></span>                                                                                          | <span data-ttu-id="ebd46-126">指定在工作到期之後，工作排程器將等待的時間量。</span><span class="sxs-lookup"><span data-stu-id="ebd46-126">Specifies the amount of time that the Task Scheduler will wait before deleting the task after it expires.</span></span><br/> |
| [<span data-ttu-id="ebd46-127">**DisallowStartIfOnBatteries**</span><span class="sxs-lookup"><span data-stu-id="ebd46-127">**DisallowStartIfOnBatteries**</span></span>](taskschedulerschema-disallowstartifonbatteries-settingstype-element.md)        | <span data-ttu-id="ebd46-128">boolean</span><span class="sxs-lookup"><span data-stu-id="ebd46-128">boolean</span></span>                                                                                           | <span data-ttu-id="ebd46-129">指定當電腦以電池執行時，工作將不會啟動。</span><span class="sxs-lookup"><span data-stu-id="ebd46-129">Specifies that the task will not be started if the computer is running on batteries.</span></span><br/>                      |
| [<span data-ttu-id="ebd46-130">**啟用**</span><span class="sxs-lookup"><span data-stu-id="ebd46-130">**Enabled**</span></span>](taskschedulerschema-enabled-settingstype-element.md)                                              | <span data-ttu-id="ebd46-131">boolean</span><span class="sxs-lookup"><span data-stu-id="ebd46-131">boolean</span></span>                                                                                           | <span data-ttu-id="ebd46-132">指定已啟用工作。</span><span class="sxs-lookup"><span data-stu-id="ebd46-132">Specifies that the task is enabled.</span></span> <span data-ttu-id="ebd46-133">只有當這項設定為 True 時，才能執行此工作。</span><span class="sxs-lookup"><span data-stu-id="ebd46-133">The task can be performed only when this setting is True.</span></span><br/>             |
| [<span data-ttu-id="ebd46-134">**ExecutionTimeLimit**</span><span class="sxs-lookup"><span data-stu-id="ebd46-134">**ExecutionTimeLimit**</span></span>](taskschedulerschema-executiontimelimit-settingstype-element.md)                        | <span data-ttu-id="ebd46-135">duration</span><span class="sxs-lookup"><span data-stu-id="ebd46-135">duration</span></span>                                                                                          | <span data-ttu-id="ebd46-136">允許完成工作的時間量。</span><span class="sxs-lookup"><span data-stu-id="ebd46-136">Amount of time allowed to complete the task.</span></span><br/>                                                              |
| [<span data-ttu-id="ebd46-137">**Hidden**</span><span class="sxs-lookup"><span data-stu-id="ebd46-137">**Hidden**</span></span>](taskschedulerschema-hidden-settingstype-element.md)                                                | <span data-ttu-id="ebd46-138">boolean</span><span class="sxs-lookup"><span data-stu-id="ebd46-138">boolean</span></span>                                                                                           | <span data-ttu-id="ebd46-139">指定預設情況下，工作將不會顯示在 UI 中。</span><span class="sxs-lookup"><span data-stu-id="ebd46-139">Specifies that the task will not be visible in the UI by default.</span></span><br/>                                         |
| [<span data-ttu-id="ebd46-140">**IdleSettings**</span><span class="sxs-lookup"><span data-stu-id="ebd46-140">**IdleSettings**</span></span>](taskschedulerschema-idlesettings-settingstype-element.md)                                    | [<span data-ttu-id="ebd46-141">**idleSettingsType**</span><span class="sxs-lookup"><span data-stu-id="ebd46-141">**idleSettingsType**</span></span>](taskschedulerschema-idlesettingstype-complextype.md)                      | <span data-ttu-id="ebd46-142">指定當電腦處於閒置狀態時，工作排程器如何執行工作。</span><span class="sxs-lookup"><span data-stu-id="ebd46-142">Specifies how the Task Scheduler performs tasks when the computer is in an idle state.</span></span><br/>                    |
| [<span data-ttu-id="ebd46-143">**MaintenanceSettings**</span><span class="sxs-lookup"><span data-stu-id="ebd46-143">**MaintenanceSettings**</span></span>](taskschedulerschema-maintenancesettings-maintenancesettingstype-element.md)           | [<span data-ttu-id="ebd46-144">**maintenanceSettingsType**</span><span class="sxs-lookup"><span data-stu-id="ebd46-144">**maintenanceSettingsType**</span></span>](taskschedulerschema-maintenancesettingstype-complextype.md)        | <span data-ttu-id="ebd46-145">指定工作排程器在自動維護期間如何執行工作。</span><span class="sxs-lookup"><span data-stu-id="ebd46-145">Specifies how the Task Scheduler performs tasks during Automatic maintenance.</span></span><br/>                             |
| [<span data-ttu-id="ebd46-146">**MultipleInstancesPolicy**</span><span class="sxs-lookup"><span data-stu-id="ebd46-146">**MultipleInstancesPolicy**</span></span>](taskschedulerschema-multipleinstancespolicy-settingstype-element.md)              | [<span data-ttu-id="ebd46-147">**multipleInstancesPolicyType**</span><span class="sxs-lookup"><span data-stu-id="ebd46-147">**multipleInstancesPolicyType**</span></span>](taskschedulerschema-multipleinstancespolicytype-simpletype.md) | <span data-ttu-id="ebd46-148">指定原則，定義工作排程器處理工作之多個實例的方式。</span><span class="sxs-lookup"><span data-stu-id="ebd46-148">Specifies the policy that defines how the Task Scheduler deals with multiple instances of the task.</span></span><br/>       |
| [<span data-ttu-id="ebd46-149">**優先順序**</span><span class="sxs-lookup"><span data-stu-id="ebd46-149">**Priority**</span></span>](taskschedulerschema-priority-settingstype-element.md)                                            | [<span data-ttu-id="ebd46-150">**priorityType**</span><span class="sxs-lookup"><span data-stu-id="ebd46-150">**priorityType**</span></span>](taskschedulerschema-prioritytype-simpletype.md)                               | <span data-ttu-id="ebd46-151">指定工作的優先權層級。</span><span class="sxs-lookup"><span data-stu-id="ebd46-151">Specifies the priority level for the task.</span></span><br/>                                                                |
| [<span data-ttu-id="ebd46-152">**RestartOnFailure**</span><span class="sxs-lookup"><span data-stu-id="ebd46-152">**RestartOnFailure**</span></span>](taskschedulerschema-restartonfailure-settingstype-element.md)                            | [<span data-ttu-id="ebd46-153">**restartType**</span><span class="sxs-lookup"><span data-stu-id="ebd46-153">**restartType**</span></span>](taskschedulerschema-restarttype-complextype.md)                                | <span data-ttu-id="ebd46-154">指定當工作因為任何原因而失敗時，工作排程器將嘗試重新開機工作。</span><span class="sxs-lookup"><span data-stu-id="ebd46-154">Specifies that the Task Scheduler will attempt to restart the task if the task fails for any reason.</span></span><br/>      |
| [<span data-ttu-id="ebd46-155">**RunOnlyIfIdle**</span><span class="sxs-lookup"><span data-stu-id="ebd46-155">**RunOnlyIfIdle**</span></span>](taskschedulerschema-runonlyifidle-settingstype-element.md)                                  | <span data-ttu-id="ebd46-156">boolean</span><span class="sxs-lookup"><span data-stu-id="ebd46-156">boolean</span></span>                                                                                           | <span data-ttu-id="ebd46-157">指定只有當電腦處於閒置狀態時，才會執行工作。</span><span class="sxs-lookup"><span data-stu-id="ebd46-157">Specifies that the task is run only when the computer is in an idle state.</span></span><br/>                                |
| [<span data-ttu-id="ebd46-158">**RunOnlyIfNetworkAvailable**</span><span class="sxs-lookup"><span data-stu-id="ebd46-158">**RunOnlyIfNetworkAvailable**</span></span>](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md)          | <span data-ttu-id="ebd46-159">boolean</span><span class="sxs-lookup"><span data-stu-id="ebd46-159">boolean</span></span>                                                                                           | <span data-ttu-id="ebd46-160">指定只有在有可用的網路時，工作排程器才會執行工作。</span><span class="sxs-lookup"><span data-stu-id="ebd46-160">Specifies that the Task Scheduler will run the task only when a network is available.</span></span><br/>                     |
| [<span data-ttu-id="ebd46-161">**StartWhenAvailable**</span><span class="sxs-lookup"><span data-stu-id="ebd46-161">**StartWhenAvailable**</span></span>](taskschedulerschema-startwhenavailable-settingstype-element.md)                        | <span data-ttu-id="ebd46-162">boolean</span><span class="sxs-lookup"><span data-stu-id="ebd46-162">boolean</span></span>                                                                                           | <span data-ttu-id="ebd46-163">指定工作排程器可以在經過排程的時間之後隨時啟動工作。</span><span class="sxs-lookup"><span data-stu-id="ebd46-163">Specifies that the Task Scheduler can start the task at any time after its scheduled time has passed.</span></span><br/>     |
| [<span data-ttu-id="ebd46-164">**StopIfGoingOnBatteries (settingsType)**</span><span class="sxs-lookup"><span data-stu-id="ebd46-164">**StopIfGoingOnBatteries (settingsType)**</span></span>](taskschedulerschema-stopifgoingonbatteries-settingstype-element.md) | <span data-ttu-id="ebd46-165">boolean</span><span class="sxs-lookup"><span data-stu-id="ebd46-165">boolean</span></span>                                                                                           | <span data-ttu-id="ebd46-166">指定當電腦進入電池時，工作將會停止。</span><span class="sxs-lookup"><span data-stu-id="ebd46-166">Specifies that the task will be stopped if the computer is going onto batteries.</span></span><br/>                          |
| [<span data-ttu-id="ebd46-167">**揮發 性**</span><span class="sxs-lookup"><span data-stu-id="ebd46-167">**Volatile**</span></span>](taskschedulerschema-volatile-element.md)                                                         | <span data-ttu-id="ebd46-168">boolean</span><span class="sxs-lookup"><span data-stu-id="ebd46-168">boolean</span></span>                                                                                           | <span data-ttu-id="ebd46-169">指定在 Windows 啟動時工作排程器是否自動停用工作。</span><span class="sxs-lookup"><span data-stu-id="ebd46-169">Specifies if the task is automatically disabled by Task Scheduler at Windows startup.</span></span><br/>                     |
| [<span data-ttu-id="ebd46-170">**WakeToRun (settingsType)**</span><span class="sxs-lookup"><span data-stu-id="ebd46-170">**WakeToRun (settingsType)**</span></span>](taskschedulerschema-waketorun-settingstype-element.md)                           | <span data-ttu-id="ebd46-171">boolean</span><span class="sxs-lookup"><span data-stu-id="ebd46-171">boolean</span></span>                                                                                           | <span data-ttu-id="ebd46-172">指定工作排程器會在執行工作時喚醒電腦。</span><span class="sxs-lookup"><span data-stu-id="ebd46-172">Specifies that Task Scheduler will wake the computer when it is time to run the task.</span></span><br/>                     |



## <a name="remarks"></a><span data-ttu-id="ebd46-173">備註</span><span class="sxs-lookup"><span data-stu-id="ebd46-173">Remarks</span></span>

<span data-ttu-id="ebd46-174">您可以選取上述的一或多個子項目。</span><span class="sxs-lookup"><span data-stu-id="ebd46-174">You can select one or more of the child elements referenced above.</span></span>

<span data-ttu-id="ebd46-175">針對 c + + 開發，會使用 [**ITaskDefinition 的 Settings 屬性**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_settings)來指定工作的註冊資訊。</span><span class="sxs-lookup"><span data-stu-id="ebd46-175">For C++ development, the registration information of a task is specified using the [**Settings property of ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_settings).</span></span>

<span data-ttu-id="ebd46-176">針對開發腳本，會使用 [ [**TaskDefinition**](taskdefinition-settings.md) ] 屬性來指定工作的註冊資訊。</span><span class="sxs-lookup"><span data-stu-id="ebd46-176">For scripting development, the registration information of a task is specified using the [**TaskDefinition.Settings**](taskdefinition-settings.md) property.</span></span>

## <a name="examples"></a><span data-ttu-id="ebd46-177">範例</span><span class="sxs-lookup"><span data-stu-id="ebd46-177">Examples</span></span>

<span data-ttu-id="ebd46-178">下列 XML 程式碼範例會定義允許工作的永久終止的設定元素。</span><span class="sxs-lookup"><span data-stu-id="ebd46-178">The following XML code example defines a settings element that allows a hard termination of the task.</span></span>


```XML
<task>
    <Settings>
        <AllowHardTerminate>true</AllowHardTerminate>
        <AllowStartOnDemand>true</AllowStartOnDemand>
    </Settings>
</task>
```



<span data-ttu-id="ebd46-179">如需設定工作設定之 XML 的詳細資訊和完整範例，請參閱 [時間觸發程式範例 (xml) ](time-trigger-example--xml-.md)。</span><span class="sxs-lookup"><span data-stu-id="ebd46-179">For more information and a complete example of the XML for setting task settings, see [Time Trigger Example (XML)](time-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ebd46-180">規格需求</span><span class="sxs-lookup"><span data-stu-id="ebd46-180">Requirements</span></span>



| <span data-ttu-id="ebd46-181">需求</span><span class="sxs-lookup"><span data-stu-id="ebd46-181">Requirement</span></span> | <span data-ttu-id="ebd46-182">值</span><span class="sxs-lookup"><span data-stu-id="ebd46-182">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ebd46-183">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ebd46-183">Minimum supported client</span></span><br/> | <span data-ttu-id="ebd46-184">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ebd46-184">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ebd46-185">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ebd46-185">Minimum supported server</span></span><br/> | <span data-ttu-id="ebd46-186">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ebd46-186">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ebd46-187">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ebd46-187">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebd46-188">工作排程器架構元素</span><span class="sxs-lookup"><span data-stu-id="ebd46-188">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="ebd46-189">工作排程器</span><span class="sxs-lookup"><span data-stu-id="ebd46-189">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





