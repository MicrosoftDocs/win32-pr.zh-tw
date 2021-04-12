---
title: ScheduleByWeek (calendarTriggerType) 元素
description: 指定每週排程。
ms.assetid: d2c33e76-0564-4b3c-ab86-e7bca667fa4f
keywords:
- 每週觸發程式工作排程器、XML 元素
- ScheduleByWeek 元素工作排程器
topic_type:
- apiref
api_name:
- ScheduleByWeek
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2d5ab62a0c39c4c1d0102edcdb96d310e9315820
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385182"
---
# <a name="schedulebyweek-calendartriggertype-element"></a>ScheduleByWeek (calendarTriggerType) 元素

指定每週排程。 例如，工作會在每週的特定一天或每隔一周的特定一天，于上午8:00 開始。

``` syntax
<xs:element name="ScheduleByWeek"
    type="weeklyScheduleType"
 />
```

**ScheduleByWeek** 元素是由 [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md)複雜型別定義。

## <a name="parent-element"></a>父元素



| 元素                                                                             | 衍生自                                                                       | Description                                                                                |
|-------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md) | [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md) | 指定每日、每週、每月或每週 (DOW) 觸發程式。<br/> |



## <a name="child-elements"></a>子元素



| 元素                                                                               | 類型                                                                     | Description                                                          |
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------------|----------------------------------------------------------------------|
| [**DaysOfWeek**](taskschedulerschema-daysofweek-weeklyscheduletype-element.md)       | [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) | 指定工作執行的星期幾。<br/>    |
| [**WeeksInterval**](taskschedulerschema-weeksinterval-weeklyscheduletype-element.md) | unsignedByte                                                             | 指定排程中周之間的間隔。<br/> |



## <a name="remarks"></a>備註

上方所列的子專案是由 [**weeklyScheduleType**](taskschedulerschema-weeklyscheduletype-complextype.md) 複雜元素類型所定義。

工作開始的當日時間是由 [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) 元素設定。

針對開發腳本，會使用 [**WeeklyTrigger**](weeklytrigger.md) 物件指定每週觸發程式。

針對 c + + 開發，每週觸發程式都是使用 [**IWeeklyTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iweeklytrigger) 介面指定。

## <a name="examples"></a>範例

下列 XML 定義每週的行事曆觸發程式，從星期一到星期五的上午 8:00 (開始工作) 。


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

 

 





