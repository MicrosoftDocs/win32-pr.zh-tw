---
title: MonthlyDOWTrigger 物件
description: 代表觸發程式的腳本物件，此觸發程式會在每個月的每週工作日排程啟動工作。
ms.assetid: 18607189-295f-4f7d-bf72-f0ac8d5067cf
keywords:
- 每月 DOW 觸發程式工作排程器，物件
- MonthlyDOWTrigger 物件工作排程器
- MonthlyDOWTrigger 物件工作排程器，說明
topic_type:
- apiref
api_name:
- MonthlyDOWTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b7e43925c6ebe27933a39fe5e25f37ffe6cf72e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024886"
---
# <a name="monthlydowtrigger-object"></a>MonthlyDOWTrigger 物件

代表觸發程式的腳本物件，此觸發程式會在每個月的每週工作日排程啟動工作。 例如，工作會在每個第一個星期四開始，可能到10月。

## <a name="members"></a>成員

**MonthlyDOWTrigger** 物件具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**MonthlyDOWTrigger** 物件具有這些屬性。



| 屬性                                                                          | 存取類型           | Description                                                                                                                                                                                 |
|:----------------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DaysOfWeek**](monthlydowtrigger-daysofweek.md)<br/>                     | 讀取/寫入<br/> | 取得或設定工作在一周中的哪幾天執行。<br/>                                                                                                                    |
| [**啟用**](trigger-enabled.md)<br/>                                     | 讀取/寫入<br/> | 繼承自 [**觸發**](trigger.md) 程式物件。 取得或設定布林值，這個值會指出是否已啟用觸發程式。<br/>                                                |
| [EndBoundary](trigger-endboundary.md)<br/>                                 | 讀取/寫入<br/> | 繼承自 [**觸發**](trigger.md) 程式物件。 取得或設定停用觸發程式的日期和時間。 觸發程式在停用之後無法啟動工作。<br/> |
| [**ExecutionTimeLimit**](trigger-executiontimelimit.md)<br/>               | 讀取/寫入<br/> | 繼承自 [**觸發**](trigger.md) 程式物件。 取得或設定允許執行此觸發程式之工作的最大時間量。<br/>                          |
| [**Id**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                              | 讀取/寫入<br/> | 繼承自 [**觸發**](trigger.md) 程式物件。 取得或設定觸發程式的識別碼。<br/>                                                                               |
| [**MonthsOfYear**](monthlydowtrigger-monthsofyear.md)<br/>                 | 讀取/寫入<br/> | 取得或設定工作在一年中執行的月份。<br/>                                                                                                                  |
| [**RandomDelay**](monthlydowtrigger-randomdelay.md)<br/>                   | 讀取/寫入<br/> | 取得或設定隨機加入至觸發程式開始時間的延遲時間。<br/>                                                                                               |
| [**重複**](trigger-repetition.md)<br/>                               | 讀取/寫入<br/> | 繼承自 [**觸發**](trigger.md) 程式物件。 取得或設定工作的執行頻率，以及啟動工作之後重複模式重複的時間長度。<br/>          |
| [**RunOnLastWeekOfMonth**](monthlydowtrigger-runonlastweekofmonth.md)<br/> | 讀取/寫入<br/> | 取得或設定布林值，指出工作會在當月的最後一周執行。<br/>                                                                                    |
| [**StartBoundary**](trigger-startboundary.md)<br/>                         | 讀取/寫入<br/> | 繼承自 [**觸發**](trigger.md) 程式物件。 取得或設定啟動觸發程式的日期和時間。<br/>                                                              |
| [**類型**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                                          | 唯讀<br/>  | 繼承自 [**觸發**](trigger.md) 程式物件。 取得觸發程式的類型。<br/>                                                                                              |
| [**WeeksOfMonth**](monthlydowtrigger-weeksofmonth.md)<br/>                 | 讀取/寫入<br/> | 取得或設定工作執行的月份周數。<br/>                                                                                                                  |



 

## <a name="remarks"></a>備註

工作開始的當日時間是由 [**StartBoundary**](trigger-startboundary.md) 屬性所設定。

在讀取或寫入工作的 XML 時，會使用工作排程器架構的 [**ScheduleByMonthDayOfWeek**](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) 元素來指定每週的星期幾觸發程式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                    |
| 類型程式庫<br/>             | <dl> <dt>Taskschd.msc .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**觸發**](trigger.md)
</dt> <dt>

[工作排程器物件](task-scheduler-objects.md)
</dt> <dt>

[工作排程器](task-scheduler-start-page.md)
</dt> <dt>

[**TriggerCollection**](triggercollection.md)
</dt> <dt>

[**TriggerCollection 建立**](triggercollection-create.md)
</dt> </dl>

 

 





