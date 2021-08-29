---
title: MonthlyTrigger 物件
description: 腳本物件，代表根據每月排程啟動工作的觸發程式。
ms.assetid: d73715cb-a52e-4daf-930f-e94fbe28881e
keywords:
- 每月觸發程式工作排程器，物件
- MonthlyTrigger 物件工作排程器
- MonthlyTrigger 物件工作排程器，說明
topic_type:
- apiref
api_name:
- MonthlyTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 078ecf023bd66fb0ad92b87f6dcc16978166fd7c6b3bbfce6d9b971f19b87be9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117760065"
---
# <a name="monthlytrigger-object"></a>MonthlyTrigger 物件

腳本物件，代表根據每月排程啟動工作的觸發程式。 例如，工作會在特定月份的特定日子開始。

## <a name="members"></a>成員

**MonthlyTrigger** 物件具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**MonthlyTrigger** 物件具有這些屬性。



| 屬性                                                                     | 存取類型           | 描述                                                                                                                                                                                 |
|:-----------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DaysOfMonth**](monthlytrigger-daysofmonth.md)<br/>                 | 讀取/寫入<br/> | 取得或設定工作執行的當月天數。<br/>                                                                                                                   |
| [**啟用**](trigger-enabled.md)<br/>                                | 讀取/寫入<br/> | 繼承自 [**觸發**](trigger.md) 程式物件。 取得或設定布林值，這個值會指出是否已啟用觸發程式。<br/>                                                |
| [EndBoundary](trigger-endboundary.md)<br/>                            | 讀取/寫入<br/> | 繼承自 [**觸發**](trigger.md) 程式物件。 取得或設定停用觸發程式的日期和時間。 觸發程式在停用之後無法啟動工作。<br/> |
| [**ExecutionTimeLimit**](trigger-executiontimelimit.md)<br/>          | 讀取/寫入<br/> | 繼承自 [**觸發**](trigger.md) 程式物件。 取得或設定允許執行觸發程式之工作的最大時間量。<br/>                           |
| [**Id**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                         | 讀取/寫入<br/> | 繼承自 [**觸發**](trigger.md) 程式物件。 取得或設定觸發程式的識別碼。<br/>                                                                               |
| [**MonthsOfYear**](monthlytrigger-monthsofyear.md)<br/>               | 讀取/寫入<br/> | 取得或設定工作在一年中執行的月份。<br/>                                                                                                                  |
| [**RandomDelay**](monthlytrigger-randomdelay.md)<br/>                 | 讀取/寫入<br/> | 取得或設定隨機加入至觸發程式開始時間的延遲時間。<br/>                                                                                               |
| [**重複**](trigger-repetition.md)<br/>                          | 讀取/寫入<br/> | 繼承自 [**觸發**](trigger.md) 程式物件。 取得或設定工作的執行頻率，以及啟動工作之後重複模式重複的時間長度。<br/>          |
| [**RunOnLastDayOfMonth**](monthlytrigger-runonlastdayofmonth.md)<br/> | 讀取/寫入<br/> | 取得或設定布林值，指出工作會在當月的最後一天執行。<br/>                                                                                     |
| [**StartBoundary**](trigger-startboundary.md)<br/>                    | 讀取/寫入<br/> | 繼承自 [**觸發**](trigger.md) 程式物件。 取得或設定啟動觸發程式的日期和時間。<br/>                                                              |
| [**類型**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                                     | 唯讀<br/>  | 繼承自 [**觸發**](trigger.md) 程式物件。 取得觸發程式的類型。<br/>                                                                                              |



 

## <a name="remarks"></a>備註

工作開始的當日時間是由 [**StartBoundary**](trigger-startboundary.md) 屬性所設定。

針對工作讀取或撰寫您自己的 XML 時，會使用工作排程器架構的 [**ScheduleByMonth**](taskschedulerschema-schedulebymonth-calendartriggertype-element.md) 元素來指定每月觸發程式。

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
</dt> <dt>

[**TriggerCollection**](triggercollection.md)
</dt> <dt>

[**TriggerCollection 建立**](triggercollection-create.md)
</dt> </dl>

 

 





