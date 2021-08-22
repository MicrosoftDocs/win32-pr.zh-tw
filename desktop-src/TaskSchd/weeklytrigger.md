---
title: WeeklyTrigger 物件
description: 腳本物件，代表根據每週排程啟動工作的觸發程式。
ms.assetid: a000d7a8-0239-440f-b49b-7f0c55b01e8e
keywords:
- 每週觸發程式工作排程器，物件
- WeeklyTrigger 物件工作排程器
- WeeklyTrigger 物件工作排程器，說明
topic_type:
- apiref
api_name:
- WeeklyTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51eb48b03efb49bd5642909af4b99b99bfb1f7f139b97f8410e0d5f014843ddf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119001786"
---
# <a name="weeklytrigger-object"></a>WeeklyTrigger 物件

腳本物件，代表根據每週排程啟動工作的觸發程式。 例如，工作從上午8:00 開始。 在每週或每週的特定一天。

## <a name="members"></a>成員

**WeeklyTrigger** 物件具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**WeeklyTrigger** 物件具有這些屬性。



| 屬性                                                            | 存取類型           | 描述                                                                                                                                                                                 |
|:--------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DaysOfWeek**](weeklytrigger-daysofweek.md)<br/>           | 讀取/寫入<br/> | 取得或設定工作在一周中的哪幾天執行。<br/>                                                                                                                        |
| [**啟用**](trigger-enabled.md)<br/>                       | 讀取/寫入<br/> | 繼承自 [**觸發**](trigger.md) 程式物件。 取得或設定布林值，這個值會指出是否已啟用觸發程式。<br/>                                                |
| [**EndBoundary**](trigger-endboundary.md)<br/>               | 讀取/寫入<br/> | 繼承自 [**觸發**](trigger.md) 程式物件。 取得或設定停用觸發程式的日期和時間。 觸發程式在停用之後無法啟動工作。<br/> |
| [**ExecutionTimeLimit**](trigger-executiontimelimit.md)<br/> | 讀取/寫入<br/> | 繼承自 [**觸發**](trigger.md) 程式物件。 取得或設定允許執行觸發程式之工作的最大時間量。<br/>                           |
| [**Id**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                | 讀取/寫入<br/> | 繼承自 [**觸發**](trigger.md) 程式物件。 取得或設定觸發程式的識別碼。<br/>                                                                               |
| [**RandomDelay**](weeklytrigger-randomdelay.md)<br/>         | 讀取/寫入<br/> | 取得或設定隨機加入至觸發程式開始時間的延遲時間。<br/>                                                                                               |
| [**重複**](trigger-repetition.md)<br/>                 | 讀取/寫入<br/> | 繼承自 [**觸發**](trigger.md) 程式物件。 取得或設定工作的執行頻率，以及啟動工作之後重複模式重複的時間長度。<br/>          |
| [**StartBoundary**](trigger-startboundary.md)<br/>           | 讀取/寫入<br/> | 繼承自 [**觸發**](trigger.md) 程式物件。 取得或設定啟動觸發程式的日期和時間。<br/>                                                              |
| [**類型**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                            | 唯讀<br/>  | 繼承自 [**觸發**](trigger.md) 程式物件。 取得觸發程式的類型。<br/>                                                                                              |
| [**WeeksInterval**](weeklytrigger-weeksinterval.md)<br/>     | 讀取/寫入<br/> | 取得或設定排程中周之間的間隔。<br/>                                                                                                                     |



 

## <a name="remarks"></a>備註

工作開始的當日時間是由 [**StartBoundary**](trigger-startboundary.md) 屬性所設定。

針對工作讀取或撰寫您自己的 XML 時，會使用工作排程器架構的 [**ScheduleByWeek**](taskschedulerschema-schedulebyweek-calendartriggertype-element.md) 元素來指定每週觸發程式。

## <a name="examples"></a>範例

如需此腳本物件的詳細資訊和程式碼範例，請參閱 [ (腳本) 的每週觸發程式範例 ](weekly-trigger-example--scripting-.md)。

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

[**TriggerCollection**](triggercollection.md)
</dt> <dt>

[**TriggerCollection 建立**](triggercollection-create.md)
</dt> </dl>

 

 





