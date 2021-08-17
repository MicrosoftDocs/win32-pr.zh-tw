---
title: MonthlyDayOfWeekScheduleType) 元素 (周
description: 指定執行工作的月份周數。
ms.assetid: c126d1e2-6e60-4067-9fc2-86c9522cce5d
keywords:
- 周元素工作排程器
topic_type:
- apiref
api_name:
- Weeks
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 81219236012146dac54965af471412369d5c5bb34319897d4d821bb10a730aee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117757975"
---
# <a name="weeks-monthlydayofweekscheduletype-element"></a>MonthlyDayOfWeekScheduleType) 元素 (周

指定執行工作的月份周數。

``` syntax
<xs:element name="Weeks"
    type="weeksType"
 />
```

**周** 元素是由 [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md)複雜型別定義。

## <a name="parent-element"></a>父元素



| 元素                                                                                                      | 衍生自                                                                                         | 描述                                                                         |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [**ScheduleByMonthDayOfWeek**](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) | [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) | 指定在每月一周的排程上啟動工作的觸發程式。<br/> |



## <a name="child-elements"></a>子元素



| 元素                                                    | 類型                                                        | 描述                                        |
|------------------------------------------------------------|-------------------------------------------------------------|----------------------------------------------------|
| [**週**](taskschedulerschema-week-weekstype-element.md) | [**weekType**](taskschedulerschema-weektype-simpletype.md) | 指定當月的特定周。<br/> |



## <a name="remarks"></a>備註

針對開發腳本，會使用 [**MonthlyDOWTrigger WeeksOfMonth**](monthlydowtrigger-weeksofmonth.md) 屬性指定月份的周數。

若是 c + + 開發，則會使用 [**IMonthlyDOWTrigger：： WeeksOfMonth**](/windows/desktop/api/taskschd/nf-taskschd-imonthlydowtrigger-get_weeksofmonth) 屬性指定月份的周數。

指定月中的周時，請使用1-4 來指定當月的前四周，或使用 "Last" 字串來指出上周（無論是哪一周）。

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

 

 





