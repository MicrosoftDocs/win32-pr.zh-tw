---
title: 'TimeTrigger 物件 (Windows applicationmodel. .h) '
description: 代表觸發程式的腳本物件，此觸發程式會在特定的日期和時間啟動工作。
ms.assetid: 3c277827-8e70-42e7-a849-773ecc997a93
keywords:
- 時間觸發程式工作排程器，物件
- TimeTrigger 物件工作排程器
- TimeTrigger 物件工作排程器，說明
topic_type:
- apiref
api_name:
- TimeTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40f0fb6f5eaff5101f3cc1f5c4aeb2245335e4f65b27d2fafb364df2d05618ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119771978"
---
# <a name="timetrigger-object"></a>TimeTrigger 物件

代表觸發程式的腳本物件，此觸發程式會在特定的日期和時間啟動工作。

## <a name="members"></a>成員

**TimeTrigger** 物件具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**TimeTrigger** 物件具有這些屬性。



| 屬性                                                            | 存取類型           | 描述                                                                                                                                                                      |
|:--------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**啟用**](trigger-enabled.md)<br/>                       | 讀取/寫入<br/> | 繼承自 [**觸發**](trigger.md)程式。 取得或設定布林值，這個值會指出是否已啟用觸發程式。<br/>                                                |
| [**EndBoundary**](trigger-endboundary.md)<br/>               | 讀取/寫入<br/> | 繼承自 [**觸發**](trigger.md)程式。 取得或設定停用觸發程式的日期和時間。 觸發程式在停用之後無法啟動工作。<br/> |
| [**ExecutionTimeLimit**](trigger-executiontimelimit.md)<br/> | 讀取/寫入<br/> | 繼承自 [**觸發**](trigger.md)程式。 取得或設定允許執行觸發程式之工作的最大時間量。<br/>                           |
| [**Id**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                | 讀取/寫入<br/> | 繼承自 [**觸發**](trigger.md)程式。 取得或設定觸發程式的識別碼。<br/>                                                                               |
| [**RandomDelay**](dailytrigger-randomdelay.md)<br/>          | 讀取/寫入<br/> | 取得或設定隨機加入至觸發程式開始時間的延遲時間。<br/>                                                                                    |
| [**重複**](trigger-repetition.md)<br/>                 | 讀取/寫入<br/> | 繼承自 [**觸發**](trigger.md)程式。 取得或設定工作的執行頻率，以及啟動工作之後重複模式重複的時間長度。<br/>          |
| [**StartBoundary**](trigger-startboundary.md)<br/>           | 讀取/寫入<br/> | 繼承自 [**觸發**](trigger.md)程式。 取得或設定啟動觸發程式的日期和時間。 這個元素是必要的。<br/>                                    |
| [**類型**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                            | 唯讀<br/>  | 繼承自 [**觸發**](trigger.md)程式。 取得觸發程式的類型。<br/>                                                                                              |



 

## <a name="remarks"></a>備註

[**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md)元素是時間和行事曆觸發程式的必要元素， ([**TimeTrigger**](taskschedulerschema-timetrigger-triggergroup-element.md)和 [**CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md)) 。

讀取或寫入工作的 XML 時，會使用工作排程器架構的 [**TimeTrigger**](taskschedulerschema-timetrigger-triggergroup-element.md) 元素來指定閒置觸發程式。

## <a name="examples"></a>範例

如需此腳本物件的詳細資訊和範例程式碼，請參閱 [時間觸發程式範例 (腳本) ](time-trigger-example--scripting-.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                                                   |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                                             |
| 標頭<br/>                   | <dl> <dt>Windows applicationmodel.。h</dt> </dl> |
| 類型程式庫<br/>             | <dl> <dt>Taskschd.msc .tlb</dt> </dl>                          |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl>                          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**觸發程序**](trigger.md)
</dt> <dt>

[**TriggerCollection**](triggercollection.md)
</dt> <dt>

[**TriggerCollection 建立**](triggercollection-create.md)
</dt> </dl>

 

 





