---
title: monthlyDayOfWeekScheduleType 複雜類型
description: 定義 ScheduleByMonthDayOfWeek 元素的子項目和排序資訊。
ms.assetid: fb4e5ba3-592b-47a4-bedf-5181d2b7a50f
keywords:
- monthlyDayOfWeekScheduleType 複雜類型工作排程器
topic_type:
- apiref
api_name:
- monthlyDayOfWeekScheduleType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e0e15a697c07de4df59f7762e4b6dc0d167b1fff8ab7477f77f5e59d6b654f7a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119575198"
---
# <a name="monthlydayofweekscheduletype-complex-type"></a>monthlyDayOfWeekScheduleType 複雜類型

定義 [**ScheduleByMonthDayOfWeek**](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) 元素的子項目和排序資訊。

``` syntax
<xs:complexType name="monthlyDayOfWeekScheduleType">
    <xs:all>
        <xs:element name="Weeks"
            type="weeksType"
            minOccurs="0"
         />
        <xs:element name="DaysOfWeek"
            type="daysOfWeekType"
         />
        <xs:element name="Months"
            type="monthsType"
            minOccurs="0"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a>子元素



| 元素                                                                                   | 類型                                                                     | 描述                                                             |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [**DaysOfWeek**](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) | [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) | 指定工作執行的星期幾。<br/>   |
| [**月**](taskschedulerschema-months-monthlydayofweekscheduletype-element.md)         | [**monthsType**](taskschedulerschema-monthstype-complextype.md)         | 指定執行工作的年份月份。<br/> |
| [**星期**](taskschedulerschema-weeks-monthlydayofweekscheduletype-element.md)           | [**weeksType**](taskschedulerschema-weekstype-complextype.md)           | 指定執行工作的月份周數。<br/> |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[工作排程器架構複雜類型](task-scheduler-schema-complex-types.md)
</dt> <dt>

[工作排程器](task-scheduler-start-page.md)
</dt> </dl>

 

 





