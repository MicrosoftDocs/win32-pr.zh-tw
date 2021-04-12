---
title: WeeksInterval (weeklyScheduleType) 元素
description: 指定排程中周之間的間隔。
ms.assetid: 6cbf1e7e-a695-4012-97fd-fe3360c362c4
keywords:
- WeeksInterval 元素工作排程器
topic_type:
- apiref
api_name:
- WeeksInterval
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 747ca4b73ff18bdb3e29d8b909d72b8d2367d89b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385101"
---
# <a name="weeksinterval-weeklyscheduletype-element"></a>WeeksInterval (weeklyScheduleType) 元素

指定排程中周之間的間隔。

``` syntax
<xs:element name="WeeksInterval"
    minOccurs="0"
>
    <xs:simpleType>
        <xs:restriction
            base="unsignedByte"
        >
            <xs:minInclusive
                value="1"
             />
            <xs:maxInclusive
                value="52"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

元素是由 [**weeklyScheduleType**](taskschedulerschema-weeklyscheduletype-complextype.md) 複雜型別定義。

## <a name="parent-element"></a>父元素



| 元素                                                                                  | 衍生自                                                                     | Description                             |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|-----------------------------------------|
| [**ScheduleByWeek**](taskschedulerschema-schedulebyweek-calendartriggertype-element.md) | [**weeklyScheduleType**](taskschedulerschema-weeklyscheduletype-complextype.md) | 指定每週排程。<br/> |



## <a name="remarks"></a>備註

針對腳本開發，每週間隔會使用 [**WeeklyTrigger. WeeksInterval**](weeklytrigger-weeksinterval.md) 屬性來指定。

針對 c + + 開發，每週間隔是使用 [**IWeeklyTrigger：： WeeksInterval**](/windows/desktop/api/taskschd/nf-taskschd-iweeklytrigger-get_weeksinterval) 屬性來指定。

## <a name="examples"></a>範例

下列 XML 定義每週的行事曆觸發程式，從星期一到星期五的上午 8:00 ( 開始工作) 。


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

 

 





