---
title: TaskSettings 物件
description: 提供工作排程器服務用來執行工作之設定的腳本物件。
ms.assetid: f2ba952b-7864-467d-8709-eb6995dd5df5
keywords:
- TaskSettings 物件工作排程器
- TaskSettings 物件工作排程器，說明
topic_type:
- apiref
api_name:
- TaskSettings
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a687e82248598d9732e91acfd40e9f3dd4d6d3c3fe6c4954cb8706489c814126
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119738098"
---
# <a name="tasksettings-object"></a>TaskSettings 物件

提供工作排程器服務用來執行工作之設定的腳本物件。

## <a name="members"></a>成員

**TaskSettings** 物件具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**TaskSettings** 物件具有這些屬性。



| 屬性                                                                                 | 存取類型           | 描述                                                                                                                                                                                                                                                                                                                                                                                                                  |
|:-----------------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AllowDemandStart**](tasksettings-allowdemandstart.md)<br/>                     | 讀取/寫入<br/> | 取得或設定布林值，這個值表示可以使用 [執行] 命令或內容功能表來啟動工作。<br/>                                                                                                                                                                                                                                                                                     |
| [**AllowHardTerminate**](tasksettings-allowhardterminate.md)<br/>                 | 讀取/寫入<br/> | 取得或設定布林值，這個值表示工作可能會使用 [**TerminateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminateprocess)來終止。<br/>                                                                                                                                                                                                                                                                               |
| [**相容性**](tasksettings-compatibility.md)<br/>                           | 讀取/寫入<br/> | 取得或設定整數值，這個值表示與工作相容的工作排程器版本。<br/>                                                                                                                                                                                                                                                                                                           |
| [**DeleteExpiredTaskAfter**](tasksettings-deleteexpiredtaskafter.md)<br/>         | 讀取/寫入<br/> | 取得或設定在工作到期之後，工作排程器將等待的時間量。<br/>                                                                                                                                                                                                                                                                                                      |
| [**DisallowStartIfOnBatteries**](tasksettings-disallowstartifonbatteries.md)<br/> | 讀取/寫入<br/> | 取得或設定布林值，指出當電腦以電池電源執行時，不會啟動工作。<br/>                                                                                                                                                                                                                                                                                        |
| [**啟用**](tasksettings-enabled.md)<br/>                                       | 讀取/寫入<br/> | 取得或設定布林值，指出是否已啟用工作。 只有當這項設定為 True 時，才能執行此工作。<br/>                                                                                                                                                                                                                                                                                   |
| [**ExecutionTimeLimit**](tasksettings-executiontimelimit.md)<br/>                 | 讀取/寫入<br/> | 取得或設定允許完成工作的時間量。<br/>                                                                                                                                                                                                                                                                                                                                                     |
| [**Hidden**](tasksettings-hidden.md)<br/>                                         | 讀取/寫入<br/> | 取得或設定布林值，指出工作將不會顯示在 UI 中。 不過，系統管理員可以使用「主要交換器」來覆寫這項設定，讓所有工作都顯示在 UI 中。<br/>                                                                                                                                                                                           |
| [**IdleSettings**](tasksettings-idlesettings.md)<br/>                             | 讀取/寫入<br/> | 取得或設定資訊，指定當電腦處於閒置狀態時，工作排程器如何執行工作。<br/>                                                                                                                                                                                                                                                                                          |
| [**MultipleInstances**](tasksettings-multipleinstances.md)<br/>                   | 讀取/寫入<br/> | 取得或設定原則，此原則會定義工作排程器處理工作之多個實例的方式。<br/>                                                                                                                                                                                                                                                                                                            |
| [**NetworkSettings**](tasksettings-networksettings.md)<br/>                       | 讀取/寫入<br/> | 取得或設定包含網路設定檔識別碼和名稱的網路設定物件。 如果 **TaskSettings** 的 [**RunOnlyIfNetworkAvailable**](tasksettings-runonlyifnetworkavailable.md)屬性為 **True** ，而且 [**NetworkSettings**](tasksettings-networksettings.md)屬性中指定了網路 propfile，則只有在指定的網路設定檔可用時，才會執行此工作。<br/> |
| [**優先順序**](tasksettings-priority.md)<br/>                                     | 讀取/寫入<br/> | 取得或設定工作的優先權層級。<br/>                                                                                                                                                                                                                                                                                                                                                                      |
| [**RestartCount**](tasksettings-restartcount.md)<br/>                             | 讀取/寫入<br/> | 取得或設定工作排程器將嘗試重新開機工作的次數。<br/>                                                                                                                                                                                                                                                                                                                        |
| [**RestartInterval**](tasksettings-restartinterval.md)<br/>                       | 讀取/寫入<br/> | 取得或設定值，這個值會指定工作排程器嘗試重新開機工作的時間長度。<br/>                                                                                                                                                                                                                                                                                                                 |
| [**RunOnlyIfIdle**](tasksettings-runonlyifidle.md)<br/>                           | 讀取/寫入<br/> | 取得或設定布林值，這個值表示工作排程器只有在電腦處於閒置狀態時，才會執行工作。<br/>                                                                                                                                                                                                                                                                                   |
| [**RunOnlyIfNetworkAvailable**](tasksettings-runonlyifnetworkavailable.md)<br/>   | 讀取/寫入<br/> | 取得或設定布林值，這個值表示工作排程器只有在有可用的網路時才會執行工作。<br/>                                                                                                                                                                                                                                                                                           |
| [**StartWhenAvailable**](tasksettings-startwhenavailable.md)<br/>                 | 讀取/寫入<br/> | 取得或設定布林值，指出工作排程器可以在經過排程的時間之後隨時啟動工作。<br/>                                                                                                                                                                                                                                                                           |
| [**StopIfGoingOnBatteries**](tasksettings-stopifgoingonbatteries.md)<br/>         | 讀取/寫入<br/> | 取得或設定布林值，這個值表示當電腦以電池電源執行時，工作將會停止。<br/>                                                                                                                                                                                                                                                                                         |
| [**WakeToRun**](tasksettings-waketorun.md)<br/>                                   | 讀取/寫入<br/> | 取得或設定布林值，這個值表示工作排程器會在執行工作時喚醒電腦。<br/>                                                                                                                                                                                                                                                                                       |
| [**XmlText**](tasksettings-xmltext.md)<br/>                                       | 讀取/寫入<br/> | 取得或設定工作設定的 XML 格式化定義。<br/>                                                                                                                                                                                                                                                                                                                                                    |



 

## <a name="remarks"></a>備註

根據預設，工作會在開始執行時停止72小時。 您可以藉由變更 [**ExecutionTimeLimit**](tasksettings-executiontimelimit.md) 設定來變更。

讀取或寫入工作的 XML 時，工作設定會定義在工作排程器架構的 [**設定**](taskschedulerschema-settings-tasktype-element.md)元素中。

## <a name="examples"></a>範例

如需此腳本物件的詳細資訊和程式碼範例，請參閱 [時間觸發程式範例 (腳本) ](time-trigger-example--scripting-.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                    |
| 類型程式庫<br/>             | <dl> <dt>Taskschd.msc .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[工作排程器](task-scheduler-start-page.md)
</dt> <dt>

[**TaskDefinition**](taskdefinition.md)
</dt> <dt>

[**NetworkSettings**](networksettings.md)
</dt> <dt>

[**IdleSettings**](idlesettings.md)
</dt> </dl>

 

