---
title: calendarTriggerType 複雜類型
description: 定義月曆元素的子項目和排序資訊。
ms.assetid: bf0d964e-aff2-4807-b086-c504f8963663
keywords:
- calendarTriggerType 複雜類型工作排程器
topic_type:
- apiref
api_name:
- calendarTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6f45434fa68b6300157a29318ba257f43bac5992
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106976359"
---
# <a name="calendartriggertype-complex-type"></a>calendarTriggerType 複雜類型

定義月曆元素的子項目和排序資訊。

``` syntax
<xs:complexType name="calendarTriggerType">
    <xs:complexContent>
        <xs:extension
            base="triggerBaseType"
        >
            <xs:sequence>
                <xs:element name="RandomDelay"
                    type="duration"
                    default="PT0M"
                    minOccurs="0"
                 />
                <xs:choice>
                    <xs:element name="ScheduleByDay"
                        type="dailyScheduleType"
                     />
                    <xs:element name="ScheduleByWeek"
                        type="weeklyScheduleType"
                     />
                    <xs:element name="ScheduleByMonth"
                        type="monthlyScheduleType"
                     />
                    <xs:element name="ScheduleByMonthDayOfWeek"
                        type="monthlyDayOfWeekScheduleType"
                     />
                </xs:choice>
            </xs:sequence>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a>子元素



| 元素                                                                                                      | 類型                                                                                                 | Description                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**RandomDelay**](taskschedulerschema-randomdelay-calendartriggertype-element.md)                           | duration                                                                                             | 包含隨機新增至觸發程式開始時間的延遲時間。 此字串的格式為 P <days> DT <hours> H <minutes> M <seconds> S (例如，P2DT5S 是2天、5秒的延遲) 。<br/> |
| [**ScheduleByDay**](taskschedulerschema-schedulebyday-calendartriggertype-element.md)                       | [**dailyScheduleType**](taskschedulerschema-dailyscheduletype-complextype.md)                       | 指定每日排程。 例如，工作會在每天、每隔三天、每隔三天開始，依此類推。<br/>                                                                                                               |
| [**ScheduleByMonth**](taskschedulerschema-schedulebymonth-calendartriggertype-element.md)                   | [**monthlyScheduleType**](taskschedulerschema-monthlyscheduletype-complextype.md)                   | 指定每月排程。 例如，工作會在每月特定日子的特定月份從上午8:00 開始。 <br/>                                                                                                       |
| [**ScheduleByMonthDayOfWeek**](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) | [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) | 指定在每月一周的排程上啟動工作的觸發程式。 例如，工作會在一周的特定日子、每月的周數，以及當年的月份開始。 <br/>                                               |
| [**ScheduleByWeek**](taskschedulerschema-schedulebyweek-calendartriggertype-element.md)                     | [**weeklyScheduleType**](taskschedulerschema-weeklyscheduletype-complextype.md)                     | 指定每週排程。 例如，工作會在每週的特定一天或每隔一周的特定一天，于上午8:00 開始。 <br/>                                                              |



## <a name="remarks"></a>備註

除了這裡定義的子項目之外， [**CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md) 專案也會使用 [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) 複雜類型所定義的子項目。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[工作排程器架構複雜類型](task-scheduler-schema-complex-types.md)
</dt> <dt>

[工作排程器](task-scheduler-start-page.md)
</dt> </dl>

 

 





