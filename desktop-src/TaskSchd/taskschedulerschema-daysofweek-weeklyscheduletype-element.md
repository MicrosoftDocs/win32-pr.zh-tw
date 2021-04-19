---
title: DaysOfWeek (weeklyScheduleType) 元素
description: 指定工作執行的星期幾。 |DaysOfWeek (weeklyScheduleType) 元素
ms.assetid: 86555681-2324-4095-9eab-fdef40e0acba
keywords:
- DaysOfWeek 元素工作排程器
topic_type:
- apiref
api_name:
- DaysOfWeek
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3a2b310feb49f3141d1f7f08c4552305f9ffc3ea
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106998990"
---
# <a name="daysofweek-weeklyscheduletype-element"></a>DaysOfWeek (weeklyScheduleType) 元素

指定工作執行的星期幾。

``` syntax
<xs:element name="DaysOfWeek"
    type="daysOfWeekType"
 />
```

**DaysOfWeek** 元素是由 [**weeklyScheduleType**](taskschedulerschema-weeklyscheduletype-complextype.md)複雜型別定義。

## <a name="parent-element"></a>父元素



| 元素                                                                                  | 衍生自                                                                     | Description                             |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|-----------------------------------------|
| [**ScheduleByWeek**](taskschedulerschema-schedulebyweek-calendartriggertype-element.md) | [**weeklyScheduleType**](taskschedulerschema-weeklyscheduletype-complextype.md) | 指定每週排程。<br/> |



## <a name="child-elements"></a>子元素



| 元素                                                                   | 類型 | Description                                           |
|---------------------------------------------------------------------------|------|-------------------------------------------------------|
| [**星期五**](taskschedulerschema-friday-daysofweektype-element.md)       |      | 指定工作在星期五執行。<br/>    |
| [**星期一**](taskschedulerschema-monday-daysofweektype-element.md)       |      | 指定工作在星期一執行。<br/>    |
| [**星期六**](taskschedulerschema-saturday-daysofweektype-element.md)   |      | 指定工作在星期六執行。<br/>  |
| [**星期日**](taskschedulerschema-sunday-daysofweektype-element.md)       |      | 指定工作在星期日執行。<br/>    |
| [**Thursday**](taskschedulerschema-thursday-daysofweektype-element.md)   |      | 指定工作在星期四執行。<br/>  |
| [**Tuesday**](taskschedulerschema-tuesday-daysofweektype-element.md)     |      | 指定工作在星期二執行。<br/>   |
| [**星期三**](taskschedulerschema-wednesday-daysofweektype-element.md) |      | 指定工作會在星期三執行。<br/> |



## <a name="remarks"></a>備註

先前的子項目是由 [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) 複雜型別定義。

針對腳本開發，每週間隔會使用 [**WeeklyTrigger. WeeksInterval**](weeklytrigger-weeksinterval.md) 屬性來指定。

針對 c + + 開發，每週間隔是使用 [**IWeeklyTrigger：： WeeksInterval**](/windows/desktop/api/taskschd/nf-taskschd-iweeklytrigger-get_weeksinterval) 屬性來指定。

## <a name="examples"></a>範例

下列 XML 會定義每日星期一到星期五 ( 開始工作的每日日曆觸發程式，每週) 上午8:00。


```XML
<CalendarTrigger>
    <StartBoundary>2005-01-01T08:00:00</StartBoundary>
    <EndBounadry>2007-01-01T00:00:00</EndBoundary>
    <ScheduleByWeek>
        <WeeksInterval>1</WeeksInterval>
        <DaysOfWeek>
            <Monday/>
            <Tuesday/>
            <Wednesday/>
            <Thurday/>
            <Friday/>
        </DaysOfWeek>
    </ScheduleByWeek>
</CalendarTrigger>
```



如需使用每週觸發程式之工作的完整 XML 範例，請參閱 [ (xml) 的每週觸發程式範例 ](weekly-trigger-example--xml-.md)。

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

 

 





