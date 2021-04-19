---
title: settingsType 複雜類型
description: 定義 (taskType) 專案之設定的子項目和排序資訊。
ms.assetid: dba6b82d-aaa4-4f77-aeb1-c5a8f81aec25
keywords:
- settingsType 複雜類型工作排程器
topic_type:
- apiref
api_name:
- settingsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a3c2b3128a35ee0e46c56d19badd431400d4d862
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968185"
---
# <a name="settingstype-complex-type"></a><span data-ttu-id="a4827-104">settingsType 複雜類型</span><span class="sxs-lookup"><span data-stu-id="a4827-104">settingsType Complex Type</span></span>

<span data-ttu-id="a4827-105">定義 [**(taskType)**](taskschedulerschema-settings-tasktype-element.md) 專案之設定的子項目和排序資訊。</span><span class="sxs-lookup"><span data-stu-id="a4827-105">Defines the child elements and sequencing information for the [**Settings (taskType)**](taskschedulerschema-settings-tasktype-element.md) element.</span></span>

``` syntax
<xs:complexType name="settingsType">
    <xs:all>
        <xs:element name="AllowStartOnDemand"
            type="boolean"
            default="true"
            minOccurs="0"
         />
        <xs:element name="RestartOnFailure"
            type="restartType"
            minOccurs="0"
         />
        <xs:element name="MultipleInstancesPolicy"
            type="multipleInstancesPolicyType"
            default="IgnoreNew"
            minOccurs="0"
         />
        <xs:element name="DisallowStartIfOnBatteries"
            type="boolean"
            default="true"
            minOccurs="0"
         />
        <xs:element name="StopIfGoingOnBatteries"
            type="boolean"
            default="true"
            minOccurs="0"
         />
        <xs:element name="AllowHardTerminate"
            type="boolean"
            default="true"
            minOccurs="0"
         />
        <xs:element name="StartWhenAvailable"
            type="boolean"
            default="false"
            minOccurs="0"
         />
        <xs:element name="NetworkProfileName"
            type="string"
            minOccurs="0"
         />
        <xs:element name="RunOnlyIfNetworkAvailable"
            type="boolean"
            default="false"
            minOccurs="0"
         />
        <xs:element name="WakeToRun"
            type="boolean"
            default="false"
            minOccurs="0"
         />
        <xs:element name="Enabled"
            type="boolean"
            default="true"
            minOccurs="0"
         />
        <xs:element name="Hidden"
            type="boolean"
            default="false"
            minOccurs="0"
         />
        <xs:element name="DeleteExpiredTaskAfter"
            type="duration"
            default="PT0S"
            minOccurs="0"
         />
        <xs:element name="IdleSettings"
            type="idleSettingsType"
            minOccurs="0"
         />
        <xs:element name="NetworkSettings"
            type="networkSettingsType"
            minOccurs="0"
         />
        <xs:element name="ExecutionTimeLimit"
            type="duration"
            minOccurs="0"
         />
        <xs:element name="Priority"
            type="priorityType"
            default="7"
            minOccurs="0"
         />
        <xs:element name="RunOnlyIfIdle"
            type="boolean"
            default="false"
            minOccurs="0"
         />
        <xs:element name="UseUnifiedSchedulingEngine"
            type="boolean"
            default="false"
            minOccurs="0"
         />
        <xs:element name="DisallowStartOnRemoteAppSession"
            type="boolean"
            default="false"
            minOccurs="0"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="a4827-106">子元素</span><span class="sxs-lookup"><span data-stu-id="a4827-106">Child elements</span></span>



| <span data-ttu-id="a4827-107">元素</span><span class="sxs-lookup"><span data-stu-id="a4827-107">Element</span></span>                                                                                                             | <span data-ttu-id="a4827-108">類型</span><span class="sxs-lookup"><span data-stu-id="a4827-108">Type</span></span>                                                                                              | <span data-ttu-id="a4827-109">Description</span><span class="sxs-lookup"><span data-stu-id="a4827-109">Description</span></span>                                                                                                                                                                                                                                                                                                         |
|---------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a4827-110">**AllowHardTerminate**</span><span class="sxs-lookup"><span data-stu-id="a4827-110">**AllowHardTerminate**</span></span>](taskschedulerschema-allowhardterminate-settingstype-element.md)                           | <span data-ttu-id="a4827-111">boolean</span><span class="sxs-lookup"><span data-stu-id="a4827-111">boolean</span></span>                                                                                           | <span data-ttu-id="a4827-112">指定工作排程器服務是否允許對工作進行硬終止。</span><span class="sxs-lookup"><span data-stu-id="a4827-112">Specifies if the Task Scheduler service allows hard termination of the task.</span></span><br/>                                                                                                                                                                                                                             |
| [<span data-ttu-id="a4827-113">**AllowStartOnDemand**</span><span class="sxs-lookup"><span data-stu-id="a4827-113">**AllowStartOnDemand**</span></span>](taskschedulerschema-allowstartondemand-settingstype-element.md)                           | <span data-ttu-id="a4827-114">boolean</span><span class="sxs-lookup"><span data-stu-id="a4827-114">boolean</span></span>                                                                                           | <span data-ttu-id="a4827-115">指定可使用 [執行] 命令或內容功能表來啟動工作。</span><span class="sxs-lookup"><span data-stu-id="a4827-115">Specifies that the task can be started by using either the Run command or the Context menu.</span></span> <br/>                                                                                                                                                                                                             |
| [<span data-ttu-id="a4827-116">**DeleteExpiredTaskAfter**</span><span class="sxs-lookup"><span data-stu-id="a4827-116">**DeleteExpiredTaskAfter**</span></span>](taskschedulerschema-deleteexpiredtaskafter-settingstype-element.md)                   | <span data-ttu-id="a4827-117">duration</span><span class="sxs-lookup"><span data-stu-id="a4827-117">duration</span></span>                                                                                          | <span data-ttu-id="a4827-118">指定在工作到期之後，工作排程器將等待的時間量。</span><span class="sxs-lookup"><span data-stu-id="a4827-118">Specifies the amount of time that the Task Scheduler will wait before deleting the task after it expires.</span></span> <span data-ttu-id="a4827-119">如果未指定這個專案的值，工作排程器服務將不會刪除該工作。</span><span class="sxs-lookup"><span data-stu-id="a4827-119">If no value is specified for this element, then the Task Scheduler service will not delete the task.</span></span><br/>                                                                                           |
| [<span data-ttu-id="a4827-120">**DisallowStartIfOnBatteries**</span><span class="sxs-lookup"><span data-stu-id="a4827-120">**DisallowStartIfOnBatteries**</span></span>](taskschedulerschema-disallowstartifonbatteries-settingstype-element.md)           | <span data-ttu-id="a4827-121">boolean</span><span class="sxs-lookup"><span data-stu-id="a4827-121">boolean</span></span>                                                                                           | <span data-ttu-id="a4827-122">指定當電腦以電池電源執行時，工作將不會啟動。</span><span class="sxs-lookup"><span data-stu-id="a4827-122">Specifies that the task will not be started if the computer is running on battery power.</span></span><br/>                                                                                                                                                                                                                 |
| [<span data-ttu-id="a4827-123">**DisallowStartOnRemoteAppSession**</span><span class="sxs-lookup"><span data-stu-id="a4827-123">**DisallowStartOnRemoteAppSession**</span></span>](taskschedulerschema-disallowstartonremoteappsession-settingstype-element.md) | <span data-ttu-id="a4827-124">boolean</span><span class="sxs-lookup"><span data-stu-id="a4827-124">boolean</span></span>                                                                                           | <span data-ttu-id="a4827-125">指定當工作觸發為在本機上整合 (滑軌) 會話的遠端應用程式中執行時，不應該啟動工作。</span><span class="sxs-lookup"><span data-stu-id="a4827-125">Specifies that the task should not start if the task is triggered to run in a Remote Applications Integrated Locally (RAIL) session.</span></span><br/>                                                                                                                                                                     |
| [<span data-ttu-id="a4827-126">**啟用**</span><span class="sxs-lookup"><span data-stu-id="a4827-126">**Enabled**</span></span>](taskschedulerschema-enabled-settingstype-element.md)                                                 | <span data-ttu-id="a4827-127">boolean</span><span class="sxs-lookup"><span data-stu-id="a4827-127">boolean</span></span>                                                                                           | <span data-ttu-id="a4827-128">指定已啟用工作。</span><span class="sxs-lookup"><span data-stu-id="a4827-128">Specifies that the task is enabled.</span></span> <span data-ttu-id="a4827-129">只有當這項設定為 **True** 時，才能執行此工作。</span><span class="sxs-lookup"><span data-stu-id="a4827-129">The task can be performed only when this setting is **True**.</span></span><br/>                                                                                                                                                                                                        |
| [<span data-ttu-id="a4827-130">**ExecutionTimeLimit**</span><span class="sxs-lookup"><span data-stu-id="a4827-130">**ExecutionTimeLimit**</span></span>](taskschedulerschema-executiontimelimit-settingstype-element.md)                           | <span data-ttu-id="a4827-131">duration</span><span class="sxs-lookup"><span data-stu-id="a4827-131">duration</span></span>                                                                                          | <span data-ttu-id="a4827-132">指定允許完成工作的時間量。</span><span class="sxs-lookup"><span data-stu-id="a4827-132">Specifies the amount of time allowed to complete the task.</span></span><br/>                                                                                                                                                                                                                                               |
| [<span data-ttu-id="a4827-133">**Hidden**</span><span class="sxs-lookup"><span data-stu-id="a4827-133">**Hidden**</span></span>](taskschedulerschema-hidden-settingstype-element.md)                                                   | <span data-ttu-id="a4827-134">boolean</span><span class="sxs-lookup"><span data-stu-id="a4827-134">boolean</span></span>                                                                                           | <span data-ttu-id="a4827-135">依預設，指定工作不會在使用者介面中顯示 (UI) 。</span><span class="sxs-lookup"><span data-stu-id="a4827-135">Specifies, by default, that the task will not be visible in the user interface (UI).</span></span><br/>                                                                                                                                                                                                                     |
| [<span data-ttu-id="a4827-136">**IdleSettings**</span><span class="sxs-lookup"><span data-stu-id="a4827-136">**IdleSettings**</span></span>](taskschedulerschema-idlesettings-settingstype-element.md)                                       | [<span data-ttu-id="a4827-137">**idleSettingsType**</span><span class="sxs-lookup"><span data-stu-id="a4827-137">**idleSettingsType**</span></span>](taskschedulerschema-idlesettingstype-complextype.md)                      | <span data-ttu-id="a4827-138">指定當電腦處於閒置狀態時，工作排程器如何執行工作。</span><span class="sxs-lookup"><span data-stu-id="a4827-138">Specifies how the Task Scheduler performs tasks when the computer is in an idle state.</span></span><br/>                                                                                                                                                                                                                   |
| [<span data-ttu-id="a4827-139">**MultipleInstancesPolicy**</span><span class="sxs-lookup"><span data-stu-id="a4827-139">**MultipleInstancesPolicy**</span></span>](taskschedulerschema-multipleinstancespolicy-settingstype-element.md)                 | [<span data-ttu-id="a4827-140">**multipleInstancesPolicyType**</span><span class="sxs-lookup"><span data-stu-id="a4827-140">**multipleInstancesPolicyType**</span></span>](taskschedulerschema-multipleinstancespolicytype-simpletype.md) | <span data-ttu-id="a4827-141">指定原則，定義工作排程器處理工作之多個實例的方式。</span><span class="sxs-lookup"><span data-stu-id="a4827-141">Specifies the policy that defines how the Task Scheduler deals with multiple instances of the task.</span></span> <br/>                                                                                                                                                                                                     |
| [<span data-ttu-id="a4827-142">**NetworkProfileName**</span><span class="sxs-lookup"><span data-stu-id="a4827-142">**NetworkProfileName**</span></span>](taskschedulerschema-networkprofilename-settingstype-element.md)                           | <span data-ttu-id="a4827-143">字串</span><span class="sxs-lookup"><span data-stu-id="a4827-143">string</span></span>                                                                                            | <span data-ttu-id="a4827-144">指定網路設定檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="a4827-144">Specifies the name of a network profile.</span></span> <span data-ttu-id="a4827-145">當 [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) 元素設定為 **True** 時，工作排程器服務會驗證此網路的可用性。</span><span class="sxs-lookup"><span data-stu-id="a4827-145">The Task Scheduler service verifies the availability of this network when the [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) element is set to **True**.</span></span> <span data-ttu-id="a4827-146">此名稱會用於顯示用途。</span><span class="sxs-lookup"><span data-stu-id="a4827-146">The name is used for display purposes.</span></span><br/>        |
| [<span data-ttu-id="a4827-147">**NetworkSettings**</span><span class="sxs-lookup"><span data-stu-id="a4827-147">**NetworkSettings**</span></span>](taskschedulerschema-networksettings-settingstype-element.md)                                 | [<span data-ttu-id="a4827-148">**networkSettingsType**</span><span class="sxs-lookup"><span data-stu-id="a4827-148">**networkSettingsType**</span></span>](taskschedulerschema-networksettingstype-complextype.md)                | <span data-ttu-id="a4827-149">指定工作排程器服務用來取得網路設定檔的設定。</span><span class="sxs-lookup"><span data-stu-id="a4827-149">Specifies the settings that the Task Scheduler service uses to obtain a network profile.</span></span> <span data-ttu-id="a4827-150">當 [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) 元素設定為 **True** 時，工作排程器服務會檢查此網路的可用性。</span><span class="sxs-lookup"><span data-stu-id="a4827-150">The Task Scheduler service checks the availability of this network when the [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) element is set to **True**.</span></span><br/> |
| [<span data-ttu-id="a4827-151">**優先順序**</span><span class="sxs-lookup"><span data-stu-id="a4827-151">**Priority**</span></span>](taskschedulerschema-priority-settingstype-element.md)                                               | [<span data-ttu-id="a4827-152">**priorityType**</span><span class="sxs-lookup"><span data-stu-id="a4827-152">**priorityType**</span></span>](taskschedulerschema-prioritytype-simpletype.md)                               | <span data-ttu-id="a4827-153">指定工作的優先權層級。</span><span class="sxs-lookup"><span data-stu-id="a4827-153">Specifies the priority level for the task.</span></span><br/>                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="a4827-154">**RestartOnFailure**</span><span class="sxs-lookup"><span data-stu-id="a4827-154">**RestartOnFailure**</span></span>](taskschedulerschema-restartonfailure-settingstype-element.md)                               | [<span data-ttu-id="a4827-155">**restartType**</span><span class="sxs-lookup"><span data-stu-id="a4827-155">**restartType**</span></span>](taskschedulerschema-restarttype-complextype.md)                                | <span data-ttu-id="a4827-156">指定當工作因為任何原因而失敗時，工作排程器將嘗試重新開機工作。</span><span class="sxs-lookup"><span data-stu-id="a4827-156">Specifies that the Task Scheduler will attempt to restart the task if it fails for any reason.</span></span> <br/>                                                                                                                                                                                                          |
| [<span data-ttu-id="a4827-157">**RunOnlyIfIdle**</span><span class="sxs-lookup"><span data-stu-id="a4827-157">**RunOnlyIfIdle**</span></span>](taskschedulerschema-runonlyifidle-settingstype-element.md)                                     | <span data-ttu-id="a4827-158">boolean</span><span class="sxs-lookup"><span data-stu-id="a4827-158">boolean</span></span>                                                                                           | <span data-ttu-id="a4827-159">指定只有當電腦處於閒置狀態時，才會執行工作。</span><span class="sxs-lookup"><span data-stu-id="a4827-159">Specifies that the task is run only when the computer is in an idle state.</span></span><br/>                                                                                                                                                                                                                               |
| [<span data-ttu-id="a4827-160">**RunOnlyIfNetworkAvailable**</span><span class="sxs-lookup"><span data-stu-id="a4827-160">**RunOnlyIfNetworkAvailable**</span></span>](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md)             | <span data-ttu-id="a4827-161">boolean</span><span class="sxs-lookup"><span data-stu-id="a4827-161">boolean</span></span>                                                                                           | <span data-ttu-id="a4827-162">指定只有在有可用的網路時，工作排程器才會執行工作。</span><span class="sxs-lookup"><span data-stu-id="a4827-162">Specifies that the Task Scheduler will run the task only when a network is available.</span></span><br/>                                                                                                                                                                                                                    |
| [<span data-ttu-id="a4827-163">**StartWhenAvailable**</span><span class="sxs-lookup"><span data-stu-id="a4827-163">**StartWhenAvailable**</span></span>](taskschedulerschema-startwhenavailable-settingstype-element.md)                           | <span data-ttu-id="a4827-164">boolean</span><span class="sxs-lookup"><span data-stu-id="a4827-164">boolean</span></span>                                                                                           | <span data-ttu-id="a4827-165">指定工作排程器可以在經過排程的時間之後隨時啟動工作。</span><span class="sxs-lookup"><span data-stu-id="a4827-165">Specifies that the Task Scheduler can start the task at any time after its scheduled time has passed.</span></span><br/>                                                                                                                                                                                                    |
| [<span data-ttu-id="a4827-166">**StopIfGoingOnBatteries**</span><span class="sxs-lookup"><span data-stu-id="a4827-166">**StopIfGoingOnBatteries**</span></span>](taskschedulerschema-stopifgoingonbatteries-settingstype-element.md)                   | <span data-ttu-id="a4827-167">boolean</span><span class="sxs-lookup"><span data-stu-id="a4827-167">boolean</span></span>                                                                                           | <span data-ttu-id="a4827-168">指定當電腦切換到電池電源時，將停止工作。</span><span class="sxs-lookup"><span data-stu-id="a4827-168">Specifies that the task will be stopped if the computer switches to battery power.</span></span> <br/>                                                                                                                                                                                                                      |
| [<span data-ttu-id="a4827-169">**UseUnifiedSchedulingEngine**</span><span class="sxs-lookup"><span data-stu-id="a4827-169">**UseUnifiedSchedulingEngine**</span></span>](taskschedulerschema-useunifiedschedulingengine-settingstype-element.md)           | <span data-ttu-id="a4827-170">boolean</span><span class="sxs-lookup"><span data-stu-id="a4827-170">boolean</span></span>                                                                                           | <span data-ttu-id="a4827-171">指定使用統一排程引擎來執行工作。</span><span class="sxs-lookup"><span data-stu-id="a4827-171">Specifies that the task is run by using the Unified Scheduling Engine.</span></span><br/>                                                                                                                                                                                                                                   |
| [<span data-ttu-id="a4827-172">**WakeToRun**</span><span class="sxs-lookup"><span data-stu-id="a4827-172">**WakeToRun**</span></span>](taskschedulerschema-waketorun-settingstype-element.md)                                             | <span data-ttu-id="a4827-173">boolean</span><span class="sxs-lookup"><span data-stu-id="a4827-173">boolean</span></span>                                                                                           | <span data-ttu-id="a4827-174">指定工作排程器會在電腦執行工作之前喚醒電腦。</span><span class="sxs-lookup"><span data-stu-id="a4827-174">Specifies that Task Scheduler will wake the computer before it runs the task.</span></span><br/>                                                                                                                                                                                                                            |



## <a name="requirements"></a><span data-ttu-id="a4827-175">規格需求</span><span class="sxs-lookup"><span data-stu-id="a4827-175">Requirements</span></span>



| <span data-ttu-id="a4827-176">需求</span><span class="sxs-lookup"><span data-stu-id="a4827-176">Requirement</span></span> | <span data-ttu-id="a4827-177">值</span><span class="sxs-lookup"><span data-stu-id="a4827-177">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a4827-178">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a4827-178">Minimum supported client</span></span><br/> | <span data-ttu-id="a4827-179">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a4827-179">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a4827-180">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a4827-180">Minimum supported server</span></span><br/> | <span data-ttu-id="a4827-181">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a4827-181">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a4827-182">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a4827-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4827-183">工作排程器架構複雜類型</span><span class="sxs-lookup"><span data-stu-id="a4827-183">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="a4827-184">工作排程器</span><span class="sxs-lookup"><span data-stu-id="a4827-184">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





