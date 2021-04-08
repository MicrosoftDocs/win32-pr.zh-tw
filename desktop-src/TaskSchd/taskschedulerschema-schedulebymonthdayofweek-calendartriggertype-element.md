---
title: ScheduleByMonthDayOfWeek (calendarTriggerType) 元素
description: 指定每週的星期幾排程。
ms.assetid: 7ff17bea-fa26-40c4-90fa-d94a3690e464
keywords:
- ScheduleByMonthDayOfWeek 元素工作排程器
topic_type:
- apiref
api_name:
- ScheduleByMonthDayOfWeek
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3e92d6ad530466a2238c8239c9e262f85ae361d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686255"
---
# <a name="schedulebymonthdayofweek-calendartriggertype-element"></a>ScheduleByMonthDayOfWeek (calendarTriggerType) 元素

指定每週的星期幾排程。 例如，工作會在一周的特定日子、每月的周數，以及當年的月份開始。

``` syntax
<xs:element name="ScheduleByMonthDayOfWeek"
    type="monthlyDayOfWeekScheduleType"
 />
```

**ScheduleByMonthDayOfWeek** 元素是由 [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md)複雜型別定義。

## <a name="parent-element"></a>父元素



| 元素                                                                             | 衍生自                                                                       | Description                                                                                |
|-------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md) | [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md) | 指定每日、每週、每月或每週 (DOW) 觸發程式。<br/> |



## <a name="child-elements"></a>子元素



| 元素                                                                                   | 類型                                                                     | Description                                                             |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [**DaysOfWeek**](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) | [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) | 指定工作執行的星期幾。<br/>       |
| [**月**](taskschedulerschema-months-monthlydayofweekscheduletype-element.md)         | [**monthsType**](taskschedulerschema-monthstype-complextype.md)         | 指定執行工作的年份月份。<br/> |
| [**星期**](taskschedulerschema-weeks-monthlydayofweekscheduletype-element.md)           | unsignedByte                                                             | 指定排程中周之間的間隔。<br/>    |



## <a name="remarks"></a>備註

工作開始的當日時間是由 [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) 元素設定。

針對開發腳本，會使用 [**MonthlyDOWTrigger**](monthlydowtrigger.md) 物件來指定每月的每週工作日觸發程式。

針對 c + + 開發，會使用 [**IMonthlyDOWTrigger**](/windows/desktop/api/taskschd/nn-taskschd-imonthlydowtrigger) 介面來指定每週的星期幾觸發程式。

上方所列的子專案是由 [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) 複雜元素類型所定義。

## <a name="examples"></a>範例

下列 XML 會定義每月星期幾行事曆觸發程式，此觸發程式會在一年的每個月的第一周星期一，于) 上午8:00 點開始工作 (。


```XML
<CalendarTrigger>
    <StartBoundary>2005-01-01T08:00:00</StartBoundary>
    <EndBounadry>2007-01-01T00:00:00</EndBoundary>
    <ScheduleByMonthDayOfWeek>
        <Weeks>
            <Week>1</Week>
        </Weeks>
        <DaysOfWeek>
            <Monday/>
        </DaysOfWeek>
        <Months>
            <January/>
            <February/>
            <March/>
            <April/>
            <May/>
            <June/>
            <July/>
            <August/>
            <September/>
            <October/>
            <November/>
            <December/>
        <Months>
    </ScheduleByMonthDayOfWeek>
</CalendarTrigger>
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[工作排程器架構元素](task-scheduler-schema-elements.md)
</dt> <dt>

[工作排程器](task-scheduler-start-page.md)
</dt> </dl>

 

 





