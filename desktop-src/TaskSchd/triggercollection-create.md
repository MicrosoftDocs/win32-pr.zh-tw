---
title: TriggerCollection. Create 方法
description: 針對腳本，會為工作建立新的觸發程式。
ms.assetid: 3d7dc811-0d83-475f-8a6e-87e59dae0113
keywords:
- 觸發程式工作排程器，建立
- 建立方法工作排程器
- 建立方法工作排程器，TriggerCollection 物件
- TriggerCollection 物件工作排程器，建立方法
topic_type:
- apiref
api_name:
- TriggerCollection.Create
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7cfc32ebff941af374d2c4bb64db8ffe064961c13840e50244f416bad477a8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119001966"
---
# <a name="triggercollectioncreate-method"></a>TriggerCollection. Create 方法

針對腳本，會為工作建立新的觸發程式。

## <a name="syntax"></a>語法


```VB
TriggerCollection.Create( _
  ByVal type _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*類型* \[在\]
</dt> <dd>

此參數會設定為下列其中一個工作 [**\_ 觸發程式 \_ TYPE2**](/windows/desktop/api/taskschd/ne-taskschd-task_trigger_type2) 列舉常數。



| 值                                                                                                                                                                                                                                                                                | 意義                                                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_TRIGGER_EVENT"></span><span id="task_trigger_event"></span><dl> <dt>**工作 \_觸發程式 \_ 事件**</dt> <dt>0</dt> </dl>                                                 | 在特定事件發生時觸發工作。<br/>                                                                                                               |
| <span id="TASK_TRIGGER_TIME"></span><span id="task_trigger_time"></span><dl> <dt>**工作 \_觸發 \_ 時間**</dt> <dt>1</dt> </dl>                                                    | 在一天中的特定時間觸發工作。<br/>                                                                                                                  |
| <span id="TASK_TRIGGER_DAILY"></span><span id="task_trigger_daily"></span><dl> <dt>**工作 \_\_每日觸發**</dt>程式 <dt>2</dt> </dl>                                                 | 依每日排程觸發工作。 例如，工作會在每天、每隔三天、每隔三天的特定時間開始，依此類推。<br/>                |
| <span id="TASK_TRIGGER_WEEKLY"></span><span id="task_trigger_weekly"></span><dl> <dt>**工作 \_\_每週**</dt> <dt>3</dt>個觸發程式 </dl>                                              | 以每週排程觸發工作。 例如，工作會在每週或其他周的特定一天從上午8:00 開始。<br/>                                   |
| <span id="TASK_TRIGGER_MONTHLY"></span><span id="task_trigger_monthly"></span><dl> <dt>**工作 \_\_每月**</dt> <dt>4 個</dt>觸發程式 </dl>                                           | 依每月排程觸發工作。 例如，工作會在特定月份的特定日子開始。<br/>                                                    |
| <span id="TASK_TRIGGER_MONTHLYDOW"></span><span id="task_trigger_monthlydow"></span><dl> <dt>**工作 \_觸發程式 \_ MONTHLYDOW**</dt> <dt>5</dt> </dl>                                  | 會在每月的每週工作日排程上觸發工作。 例如，工作會在一周的特定日子、每月的周數，以及當年的月份開始。<br/> |
| <span id="TASK_TRIGGER_IDLE"></span><span id="task_trigger_idle"></span><dl> <dt>**工作 \_觸發程式 \_ 閒置**</dt> <dt>6</dt> </dl>                                                    | 當電腦進入閒置狀態時，就會觸發工作。<br/>                                                                                                  |
| <span id="TASK_TRIGGER_REGISTRATION"></span><span id="task_trigger_registration"></span><dl> <dt>**工作 \_觸發程式 \_ 註冊**</dt> <dt>7</dt> </dl>                            | 在註冊工作時觸發工作。<br/>                                                                                                                |
| <span id="TASK_TRIGGER_BOOT"></span><span id="task_trigger_boot"></span><dl> <dt>**工作 \_觸發 \_ 開機**</dt> <dt>8</dt> </dl>                                                    | 在電腦開機時觸發工作。<br/>                                                                                                                    |
| <span id="TASK_TRIGGER_LOGON"></span><span id="task_trigger_logon"></span><dl> <dt>**工作 \_觸發程式 \_ 登**</dt>入 <dt>9</dt> </dl>                                                 | 當特定使用者登入時觸發工作。<br/>                                                                                                               |
| <span id="TASK_TRIGGER_SESSION_STATE_CHANGE"></span><span id="task_trigger_session_state_change"></span><dl> <dt>**工作 \_觸發程式 \_ 會話 \_ 狀態 \_ 變更**</dt> <dt>11</dt> </dl> | 在特定會話狀態變更時觸發工作。<br/>                                                                                                      |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

代表新觸發程式的 [**觸發**](trigger.md) 程式物件。

## <a name="remarks"></a>備註

如需每個觸發程式類型的詳細資訊，請參閱 [觸發程式類型](trigger-types.md)。

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

[**觸發程序**](trigger.md)
</dt> </dl>

 

 





