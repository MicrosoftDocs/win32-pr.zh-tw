---
title: MonthlyDayOfWeekScheduleType) 元素 (月份
description: 指定在一年中的幾個月，工作會在一年中執行一周的每月日排程。
ms.assetid: 420fa7f4-7106-483e-9b3b-d1ba51f25222
keywords:
- Months 元素工作排程器
topic_type:
- apiref
api_name:
- Months
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a963032a2d33f13158af249f2b867037cf50082be005efa579148031c8e30585
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959598"
---
# <a name="months-monthlydayofweekscheduletype-element"></a>MonthlyDayOfWeekScheduleType) 元素 (月份

指定在一年中的幾個月，工作會在一年中執行一周的每月日排程。

``` syntax
<xs:element name="Months"
    type="monthsType"
 />
```

**Months** 元素是由 [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md)複雜型別定義。

## <a name="parent-element"></a>父元素



| 元素                                                                                                                            | 衍生自                                                                                         | 描述                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [**ScheduleByMonthDayOfWeek (calendarTriggerType)**](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) | [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) | 指定啟動工作的觸發程式，此觸發程式會每個月的每週工作日排程。<br/> |



## <a name="child-elements"></a>子元素



| 元素                                                               | 類型 | 描述                                           |
|-----------------------------------------------------------------------|------|-------------------------------------------------------|
| [**四月**](taskschedulerschema-april-monthstype-element.md)         |      | 指定工作會在四月執行。<br/>     |
| [**8 月**](taskschedulerschema-august-monthstype-element.md)       |      | 指定工作在8月執行。<br/>    |
| [**十二月**](taskschedulerschema-december-monthstype-element.md)   |      | 指定工作會在十二月執行。<br/>  |
| [**2 月**](taskschedulerschema-february-monthstype-element.md)   |      | 指定工作會在二月執行。<br/>  |
| [**一月**](taskschedulerschema-january-monthstype-element.md)     |      | 指定工作會在一月執行。<br/>   |
| [**7 月**](taskschedulerschema-july-monthstype-element.md)           |      | 指定工作會在七月執行。<br/>      |
| [**6 月**](taskschedulerschema-june-monthstype-element.md)           |      | 指定工作在六月執行。<br/>      |
| [**3 月**](taskschedulerschema-march-monthstype-element.md)         |      | 指定工作在三月執行。<br/>     |
| [**可能**](taskschedulerschema-may-monthstype-element.md)             |      | 指定工作在5月執行。<br/>       |
| [**十一月**](taskschedulerschema-november-monthstype-element.md)   |      | 指定工作在11月執行。<br/>  |
| [**10 月**](taskschedulerschema-october-monthstype-element.md)     |      | 指定工作在十月執行。<br/>   |
| [**9 月**](taskschedulerschema-september-monthstype-element.md) |      | 指定工作在九月執行。<br/> |



## <a name="remarks"></a>備註

在撰寫腳本時，會使用 [**MonthlyDOWTrigger. MonthsOfYear**](monthlydowtrigger-monthsofyear.md) 屬性指定一年中每月星期幾的月份。

若是 c + + 開發，則會使用 [**IMonthlyDOWTrigger：： MonthsOfYear**](/windows/desktop/api/taskschd/nf-taskschd-imonthlydowtrigger-get_monthsofyear) 屬性指定一年中每月星期幾的月份。

上述的子項目是由 [**monthsType**](taskschedulerschema-monthstype-complextype.md) 複雜型別定義。

## <a name="examples"></a>範例

下列 XML 會定義每月的每週工作日行事曆，此日曆會在每個月的第一周的星期一開始工作。


```XML
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
```



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

 

 





