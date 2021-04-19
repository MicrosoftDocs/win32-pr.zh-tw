---
title: SessionStateChangeTrigger 物件
description: 腳本物件，可觸發主控台連線或中斷連線、遠端連線或中斷連線，或工作站鎖定或解除鎖定通知的工作。
ms.assetid: ea450b8a-81cc-4d24-b850-78c967dcc5b8
keywords:
- SessionStateChangeTrigger 物件工作排程器
- SessionStateChangeTrigger 物件工作排程器，說明
topic_type:
- apiref
api_name:
- SessionStateChangeTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f55d41f495c714fe2e1798c79cc4f24b99987a49
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106995162"
---
# <a name="sessionstatechangetrigger-object"></a>SessionStateChangeTrigger 物件

腳本物件，可觸發主控台連線或中斷連線、遠端連線或中斷連線，或工作站鎖定或解除鎖定通知的工作。

## <a name="members"></a>成員

**SessionStateChangeTrigger** 物件具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**SessionStateChangeTrigger** 物件具有這些屬性。



| 屬性                                                                | 存取類型           | Description                                                                                                                                                                                               |
|:------------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**延遲**](sessionstatechangetrigger-delay.md)<br/>             | 讀取/寫入<br/> | 取得或設定值，這個值表示偵測到終端機伺服器會話狀態變更之後，啟動工作之前的延遲時間。<br/>                                         |
| [**啟用**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_enabled)<br/>                          | 讀取/寫入<br/> | 繼承自 [**觸發**](trigger.md) 程式物件。 取得或設定布林值，這個值會指出是否已啟用觸發程式。<br/>                                                              |
| [**EndBoundary**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_endboundary)<br/>                  | 讀取/寫入<br/> | 繼承自 [**觸發**](trigger.md) 程式物件。 取得或設定停用觸發程式的日期和時間。 觸發程式在停用之後無法啟動工作。<br/>               |
| [**ExecutionTimeLimit**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_executiontimelimit)<br/>    | 讀取/寫入<br/> | 繼承自 [**觸發**](trigger.md) 程式物件。 取得或設定觸發程式可啟動工作的最大時間量。<br/>                                                 |
| [**Id**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                    | 讀取/寫入<br/> | 繼承自 [**觸發**](trigger.md) 程式物件。 取得或設定觸發程式的識別碼。<br/>                                                                                             |
| [**重複**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_repetition)<br/>                    | 讀取/寫入<br/> | 繼承自 [**觸發**](trigger.md) 程式物件。 取得或設定值，這個值會指出工作的執行頻率，以及在工作啟動之後重複模式重複的時間長度。<br/> |
| [**StartBoundary**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_startboundary)<br/>              | 讀取/寫入<br/> | 繼承自 [**觸發**](trigger.md) 程式物件。 取得或設定啟動觸發程式的日期和時間。<br/>                                                                            |
| [**StateChange**](sessionstatechangetrigger-statechange.md)<br/> | 讀取/寫入<br/> | 取得或設定會觸發工作啟動的終端機伺服器會話變更類型。<br/>                                                                                                      |
| [**類型**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                                | 唯讀<br/>  | 繼承自 [**觸發**](trigger.md) 程式物件。 取得觸發程式的類型。<br/>                                                                                                            |
| [**UserId**](sessionstatechangetrigger-userid.md)<br/>           | 讀取/寫入<br/> | 取得或設定終端機伺服器會話的使用者。 當偵測到此使用者的會話狀態變更時，就會啟動工作。<br/>                                                               |



 

## <a name="remarks"></a>備註

針對工作讀取或撰寫您自己的 XML 時，會使用工作排程器架構的 [**SessionStateChangeTrigger**](taskschedulerschema-sessionstatechangetrigger-triggergroup-element.md) 元素來指定會話狀態變更觸發程式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                    |
| 類型程式庫<br/>             | <dl> <dt>Taskschd.msc .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**TriggerCollection**](triggercollection.md)
</dt> <dt>

[**TriggerCollection 建立**](triggercollection-create.md)
</dt> </dl>

 

 





