---
title: Trigger。 Type 屬性
description: 針對腳本，會取得觸發程式的類型。
ms.assetid: 346e6b02-c89e-4644-aa19-2bbf3d0fb3c3
keywords:
- Type 屬性工作排程器
- 類型屬性工作排程器，觸發程式物件
- 觸發程式物件工作排程器，類型屬性
topic_type:
- apiref
api_name:
- Trigger.Type
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bcc44e385324d161ca051b4270096e674adbba878448667ef176a9c1c63bb24b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002036"
---
# <a name="triggertype-property"></a>Trigger。 Type 屬性

針對腳本，會取得觸發程式的類型。 觸發程式類型是在建立觸發程式時定義的，而且稍後無法變更。 如需建立觸發程式的詳細資訊，請參閱 [**TriggerCollection。**](triggercollection-create.md)

## <a name="syntax"></a>Syntax


```VB
Trigger.Type As TASK_TRIGGER_TYPE2
```



## <a name="property-value"></a>屬性值

下列其中一個工作 [**\_ 觸發程式 \_ TYPE2**](/windows/desktop/api/taskschd/ne-taskschd-task_trigger_type2) 列舉值。



| 值                                                                                                                                                                                                                                                                                | 意義                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <span id="TASK_TRIGGER_EVENT"></span><span id="task_trigger_event"></span><dl> <dt>**工作 \_觸發程式 \_ 事件**</dt> <dt>0</dt> </dl>                                                 | 在特定事件發生時啟動工作。<br/>              |
| <span id="TASK_TRIGGER_TIME"></span><span id="task_trigger_time"></span><dl> <dt>**工作 \_觸發 \_ 時間**</dt> <dt>1</dt> </dl>                                                    | 在一天中的特定時間啟動工作。<br/>                 |
| <span id="TASK_TRIGGER_DAILY"></span><span id="task_trigger_daily"></span><dl> <dt>**工作 \_\_每日觸發**</dt>程式 <dt>2</dt> </dl>                                                 | 每天啟動工作。<br/>                                     |
| <span id="TASK_TRIGGER_WEEKLY"></span><span id="task_trigger_weekly"></span><dl> <dt>**工作 \_\_每週**</dt> <dt>3</dt>個觸發程式 </dl>                                              | 每週啟動工作。<br/>                                    |
| <span id="TASK_TRIGGER_MONTHLY"></span><span id="task_trigger_monthly"></span><dl> <dt>**工作 \_\_每月**</dt> <dt>4 個</dt>觸發程式 </dl>                                           | 每月啟動工作。<br/>                                   |
| <span id="TASK_TRIGGER_MONTHLYDOW"></span><span id="task_trigger_monthlydow"></span><dl> <dt>**工作 \_觸發程式 \_ MONTHLYDOW**</dt> <dt>5</dt> </dl>                                  | 在每個月于一周的特定一天啟動工作。<br/> |
| <span id="TASK_TRIGGER_IDLE"></span><span id="task_trigger_idle"></span><dl> <dt>**工作 \_觸發程式 \_ 閒置**</dt> <dt>6</dt> </dl>                                                    | 當電腦進入閒置狀態時，就會啟動工作。<br/> |
| <span id="TASK_TRIGGER_REGISTRATION"></span><span id="task_trigger_registration"></span><dl> <dt>**工作 \_觸發程式 \_ 註冊**</dt> <dt>7</dt> </dl>                            | 在註冊工作時啟動工作。<br/>               |
| <span id="TASK_TRIGGER_BOOT"></span><span id="task_trigger_boot"></span><dl> <dt>**工作 \_觸發 \_ 開機**</dt> <dt>8</dt> </dl>                                                    | 當電腦啟動時啟動工作。<br/>                   |
| <span id="TASK_TRIGGER_LOGON"></span><span id="task_trigger_logon"></span><dl> <dt>**工作 \_觸發程式 \_ 登**</dt>入 <dt>9</dt> </dl>                                                 | 在特定使用者登入時啟動工作。<br/>              |
| <span id="TASK_TRIGGER_SESSION_STATE_CHANGE"></span><span id="task_trigger_session_state_change"></span><dl> <dt>**工作 \_觸發程式 \_ 會話 \_ 狀態 \_ 變更**</dt> <dt>11</dt> </dl> | 在特定會話狀態變更時觸發工作。<br/>   |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                    |
| 類型程式庫<br/>             | <dl> <dt>Taskschd.msc .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**TriggerCollection 建立**](triggercollection-create.md)
</dt> <dt>

[**工作 \_ 觸發程式 \_ TYPE2**](/windows/desktop/api/taskschd/ne-taskschd-task_trigger_type2)
</dt> <dt>

[工作排程器](task-scheduler-start-page.md)
</dt> </dl>

 

 





