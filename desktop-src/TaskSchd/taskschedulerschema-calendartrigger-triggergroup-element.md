---
title: CalendarTrigger (triggerGroup) 元素
description: 指定每日、每週、每月或每週 (DOW) 觸發程式。
ms.assetid: 9b9218bf-222c-4ece-8b37-5c5d8b765015
keywords:
- 行事曆觸發程式工作排程器、XML 元素
- CalendarTrigger 元素工作排程器
topic_type:
- apiref
api_name:
- CalendarTrigger
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d02b14fa056940a8139e87d9b471f6eaef84c311eb095073f274a9b4adf3c6dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119516968"
---
# <a name="calendartrigger-triggergroup-element"></a>CalendarTrigger (triggerGroup) 元素

指定每日、每週、每月或每週 (DOW) 觸發程式。

``` syntax
<xs:element name="CalendarTrigger"
    type="calendarTriggerType"
 />
```

**CalendarTrigger** 元素是由 [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md)複雜型別定義。

## <a name="parent-element"></a>父元素



| 元素                                                           | 衍生自                                                         | 描述                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------|
| [**觸發程序**](taskschedulerschema-triggers-tasktype-element.md) | [**triggersType**](taskschedulerschema-triggerstype-complextype.md) | 指定啟動工作的觸發程式。<br/> |



## <a name="child-elements"></a>子元素



| 元素                                                                                                                            | 類型                                                                                                 | 描述                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [**已啟用 (triggerBaseType)**](taskschedulerschema-enabled-triggerbasetype-element.md)                                           | boolean                                                                                              | 指定啟用觸發程序。<br/>                                                                                  |
| [**EndBoundary (triggerBaseType)**](taskschedulerschema-endboundary-triggerbasetype-element.md)                                   | dateTime                                                                                             | 指定停用觸發程式的日期和時間。 觸發程式在停用之後無法啟動工作。<br/> |
| [**ExecutionTimeLimit (triggerBaseType)**](taskschedulerschema-executiontimelimit-triggerbasetype-element.md)                     | duration                                                                                             | 指定觸發程式可啟動工作的最大時間量。<br/>                                   |
| [**重複 (triggerBaseType)**](taskschedulerschema-repetition-triggerbasetype-element.md)                                     | [**repetitionType**](taskschedulerschema-repetitiontype-complextype.md)                             | 指定執行工作的頻率，以及啟動工作之後重複模式重複的時間長度。<br/>          |
| [**ScheduleByDay (calendarTriggerType)**](taskschedulerschema-schedulebyday-calendartriggertype-element.md)                       | [**dailyScheduleType**](taskschedulerschema-dailyscheduletype-complextype.md)                       | 指定每日排程。<br/>                                                                                             |
| [**ScheduleByMonth (calendarTriggerType)**](taskschedulerschema-schedulebymonth-calendartriggertype-element.md)                   | [**monthlyScheduleType**](taskschedulerschema-monthlyscheduletype-complextype.md)                   | 指定每月排程。<br/>                                                                                           |
| [**ScheduleByMonthDayOfWeek (calendarTriggerType)**](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) | [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) | 指定在每月一周的排程上啟動工作的觸發程式。<br/>                                                |
| [**ScheduleByWeek (calendarTriggerType)**](taskschedulerschema-schedulebyweek-calendartriggertype-element.md)                     | [**weeklyScheduleType**](taskschedulerschema-weeklyscheduletype-complextype.md)                     | 指定每週排程。<br/>                                                                                            |
| [**StartBoundary (triggerBaseType)**](taskschedulerschema-startboundary-triggerbasetype-element.md)                               | dateTime                                                                                             | 指定啟動觸發程式的日期和時間。 這個元素是必要的。<br/>                                    |



## <a name="attributes"></a>屬性



| 名稱 | 類型 | 描述                               |
|------|------|-------------------------------------------|
| 識別碼   | 識別碼   | 觸發程式的識別碼。<br/> |



## <a name="remarks"></a>備註

[**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md)元素是時間和行事曆觸發程式的必要元素， ([**TimeTrigger**](taskschedulerschema-timetrigger-triggergroup-element.md)和 **CalendarTrigger**) 。

上方所列的子專案是由 [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) 和 [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md) 複雜元素類型所定義。

針對腳本開發，行事曆觸發程式是使用下列其中一個物件指定的。

-   [**DailyTrigger**](dailytrigger.md)
-   [**WeeklyTrigger**](weeklytrigger.md)
-   [**MonthlyTrigger**](monthlytrigger.md)
-   [**MonthlyDOWTrigger**](monthlydowtrigger.md)

針對 c + + 開發，行事曆觸發程式是使用下列其中一個介面指定的。

-   [**IDailyTrigger**](/windows/desktop/api/taskschd/nn-taskschd-idailytrigger)
-   [**IWeeklyTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iweeklytrigger)
-   [**IMonthlyTrigger**](/windows/desktop/api/taskschd/nn-taskschd-imonthlytrigger)
-   [**IMonthlyDOWTrigger**](/windows/desktop/api/taskschd/nn-taskschd-imonthlydowtrigger)

## <a name="examples"></a>範例

如需指定行事曆觸發程式之工作的完整 XML 範例，請參閱 [ (xml) 的每日觸發程式範例 ](daily-trigger-example--xml-.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[工作排程器架構元素](task-scheduler-schema-elements.md)
</dt> <dt>

[工作排程器](task-scheduler-start-page.md)
</dt> </dl>

 

 





