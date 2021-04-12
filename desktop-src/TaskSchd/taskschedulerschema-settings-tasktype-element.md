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
# <a name="settings-tasktype-element"></a> (taskType) 元素設定

指定工作排程器用來執行工作的設定。

``` syntax
<xs:element name="Settings"
    type="settingsType"
    minOccurs="0"
 />
```

**Settings** 元素是由 [**taskType**](taskschedulerschema-tasktype-complextype.md)複雜型別定義。

## <a name="parent-element"></a>父元素



| 元素                                          | 衍生自                                                 | Description                                                                    |
|--------------------------------------------------|--------------------------------------------------------------|--------------------------------------------------------------------------------|
| [**Task**](taskschedulerschema-task-element.md) | [**taskType**](taskschedulerschema-tasktype-complextype.md) | 指定工作排程器服務所執行的工作。<br/> |



## <a name="child-elements"></a>子元素



| 元素                                                                                                          | 類型                                                                                              | Description                                                                                                          |
|------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [**AllowHardTerminate**](taskschedulerschema-allowhardterminate-settingstype-element.md)                        | boolean                                                                                           | 指定可以使用 TerminateProcess 終止工作。<br/>                                         |
| [**AllowStartOnDemand**](taskschedulerschema-allowstartondemand-settingstype-element.md)                        | boolean                                                                                           | 指定可使用 [執行] 命令或內容功能表來啟動工作。<br/>                  |
| [**DeleteExpiredTaskAfter**](taskschedulerschema-deleteexpiredtaskafter-settingstype-element.md)                | duration                                                                                          | 指定在工作到期之後，工作排程器將等待的時間量。<br/> |
| [**DisallowStartIfOnBatteries**](taskschedulerschema-disallowstartifonbatteries-settingstype-element.md)        | boolean                                                                                           | 指定當電腦以電池執行時，工作將不會啟動。<br/>                      |
| [**啟用**](taskschedulerschema-enabled-settingstype-element.md)                                              | boolean                                                                                           | 指定已啟用工作。 只有當這項設定為 True 時，才能執行此工作。<br/>             |
| [**ExecutionTimeLimit**](taskschedulerschema-executiontimelimit-settingstype-element.md)                        | duration                                                                                          | 允許完成工作的時間量。<br/>                                                              |
| [**Hidden**](taskschedulerschema-hidden-settingstype-element.md)                                                | boolean                                                                                           | 指定預設情況下，工作將不會顯示在 UI 中。<br/>                                         |
| [**IdleSettings**](taskschedulerschema-idlesettings-settingstype-element.md)                                    | [**idleSettingsType**](taskschedulerschema-idlesettingstype-complextype.md)                      | 指定當電腦處於閒置狀態時，工作排程器如何執行工作。<br/>                    |
| [**MaintenanceSettings**](taskschedulerschema-maintenancesettings-maintenancesettingstype-element.md)           | [**maintenanceSettingsType**](taskschedulerschema-maintenancesettingstype-complextype.md)        | 指定工作排程器在自動維護期間如何執行工作。<br/>                             |
| [**MultipleInstancesPolicy**](taskschedulerschema-multipleinstancespolicy-settingstype-element.md)              | [**multipleInstancesPolicyType**](taskschedulerschema-multipleinstancespolicytype-simpletype.md) | 指定原則，定義工作排程器處理工作之多個實例的方式。<br/>       |
| [**優先順序**](taskschedulerschema-priority-settingstype-element.md)                                            | [**priorityType**](taskschedulerschema-prioritytype-simpletype.md)                               | 指定工作的優先權層級。<br/>                                                                |
| [**RestartOnFailure**](taskschedulerschema-restartonfailure-settingstype-element.md)                            | [**restartType**](taskschedulerschema-restarttype-complextype.md)                                | 指定當工作因為任何原因而失敗時，工作排程器將嘗試重新開機工作。<br/>      |
| [**RunOnlyIfIdle**](taskschedulerschema-runonlyifidle-settingstype-element.md)                                  | boolean                                                                                           | 指定只有當電腦處於閒置狀態時，才會執行工作。<br/>                                |
| [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md)          | boolean                                                                                           | 指定只有在有可用的網路時，工作排程器才會執行工作。<br/>                     |
| [**StartWhenAvailable**](taskschedulerschema-startwhenavailable-settingstype-element.md)                        | boolean                                                                                           | 指定工作排程器可以在經過排程的時間之後隨時啟動工作。<br/>     |
| [**StopIfGoingOnBatteries (settingsType)**](taskschedulerschema-stopifgoingonbatteries-settingstype-element.md) | boolean                                                                                           | 指定當電腦進入電池時，工作將會停止。<br/>                          |
| [**揮發 性**](taskschedulerschema-volatile-element.md)                                                         | boolean                                                                                           | 指定在 Windows 啟動時工作排程器是否自動停用工作。<br/>                     |
| [**WakeToRun (settingsType)**](taskschedulerschema-waketorun-settingstype-element.md)                           | boolean                                                                                           | 指定工作排程器會在執行工作時喚醒電腦。<br/>                     |



## <a name="remarks"></a>備註

您可以選取上述的一或多個子項目。

針對 c + + 開發，會使用 [**ITaskDefinition 的 Settings 屬性**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_settings)來指定工作的註冊資訊。

針對開發腳本，會使用 [ [**TaskDefinition**](taskdefinition-settings.md) ] 屬性來指定工作的註冊資訊。

## <a name="examples"></a>範例

下列 XML 程式碼範例會定義允許工作的永久終止的設定元素。


```XML
<task>
    <Settings>
        <AllowHardTerminate>true</AllowHardTerminate>
        <AllowStartOnDemand>true</AllowStartOnDemand>
    </Settings>
</task>
```



如需設定工作設定之 XML 的詳細資訊和完整範例，請參閱 [時間觸發程式範例 (xml) ](time-trigger-example--xml-.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[工作排程器架構元素](task-scheduler-schema-elements.md)
</dt> <dt>

[工作排程器](task-scheduler-start-page.md)
</dt> </dl>

 

 





