---
title: IdleTrigger 物件
description: 代表觸發程式的腳本物件，此觸發程式會在發生閒置條件時啟動工作。
ms.assetid: 627d83cf-27bd-47ce-a647-fa1e9af5263e
keywords:
- 閒置觸發程式工作排程器，物件
- IdleTrigger 物件工作排程器
- IdleTrigger 物件工作排程器，說明
topic_type:
- apiref
api_name:
- IdleTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41a3c538dbd04f3eb20a86f495fcf4a8b027b51fbe5cd6443cd8ff3a69ac6ff5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119621138"
---
# <a name="idletrigger-object"></a>IdleTrigger 物件

代表觸發程式的腳本物件，此觸發程式會在發生閒置條件時啟動工作。 如需有關閒置條件的詳細資訊，請參閱工作 [閒置條件](task-idle-conditions.md)。

## <a name="members"></a>成員

**IdleTrigger** 物件具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**IdleTrigger** 物件具有這些屬性。



| 屬性                                                            | 存取類型           | 描述                                                                                                                                                                                               |
|:--------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**啟用**](trigger-enabled.md)<br/>                       | 讀取/寫入<br/> | 繼承自 [**觸發**](trigger.md) 程式物件。 取得或設定布林值，這個值會指出是否已啟用觸發程式。<br/>                                                              |
| [EndBoundary](trigger-endboundary.md)<br/>                   | 讀取/寫入<br/> | 繼承自 [**觸發**](trigger.md) 程式物件。 取得或設定停用觸發程式的日期和時間。 觸發程式在停用之後無法啟動工作。<br/>               |
| [**ExecutionTimeLimit**](trigger-executiontimelimit.md)<br/> | 讀取/寫入<br/> | 繼承自 [**觸發**](trigger.md) 程式物件。 取得或設定觸發程式可啟動工作的最大時間量。<br/>                                                 |
| [**Id**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                | 讀取/寫入<br/> | 繼承自 [**觸發**](trigger.md) 程式物件。 取得或設定觸發程式的識別碼。<br/>                                                                                             |
| [**重複**](trigger-repetition.md)<br/>                 | 讀取/寫入<br/> | 繼承自 [**觸發**](trigger.md) 程式物件。 取得或設定值，這個值會指出工作的執行頻率，以及在工作啟動之後重複模式重複的時間長度。<br/> |
| [**StartBoundary**](trigger-startboundary.md)<br/>           | 讀取/寫入<br/> | 繼承自 [**觸發**](trigger.md) 程式物件。 取得或設定啟動觸發程式的日期和時間。<br/>                                                                            |
| [**類型**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                            | 唯讀<br/>  | 繼承自 [**觸發**](trigger.md) 程式物件。 取得觸發程式的類型。<br/>                                                                                                            |



 

## <a name="remarks"></a>備註

閒置觸發程式只會在觸發程式啟動界限後進入閒置狀態時，才會觸發工作動作。

讀取或寫入工作的 XML 時，會使用工作排程器架構的 [**IdleTrigger**](taskschedulerschema-idletrigger-triggergroup-element.md) 元素來指定閒置觸發程式。

如果工作是由閒置觸發程式觸發，則會忽略 [**IdleSettings. WaitTimeout**](idlesettings-waittimeout.md) 屬性。

如果具有閒置觸發程式之工作的初始實例仍在執行中，則工作只會在沒有重複的情況下啟動一次，即使在 [ [**重複**](trigger-repetition.md) ] 屬性中定義了多個重複。 如果工作本身停止，則不會發生此行為。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                    |
| 類型程式庫<br/>             | <dl> <dt>Taskschd.msc .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**觸發程序**](trigger.md)
</dt> <dt>

[工作排程器物件](task-scheduler-objects.md)
</dt> <dt>

[工作排程器](task-scheduler-start-page.md)
</dt> </dl>

 

 





