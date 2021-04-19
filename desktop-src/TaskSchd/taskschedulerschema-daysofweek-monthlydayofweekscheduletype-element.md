---
title: DaysOfWeek (monthlyDayOfWeekScheduleType) 元素
description: 指定工作執行的星期幾。 |DaysOfWeek (monthlyDayOfWeekScheduleType) 元素
ms.assetid: d84f0019-1369-465f-9054-0fb5a83cad6d
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
ms.openlocfilehash: 3867e08dd001a035a3ab25da056f75c1e73eeeef
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106992278"
---
# <a name="daysofweek-monthlydayofweekscheduletype-element"></a>DaysOfWeek (monthlyDayOfWeekScheduleType) 元素

指定工作執行的星期幾。

``` syntax
<xs:element name="DaysOfWeek"
    type="daysOfWeekType"
 />
```

**DaysOfWeek** 元素是由 [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md)複雜型別定義。

## <a name="parent-element"></a>父元素



| 元素                                                                                                      | 衍生自                                                                                         | Description                                                                          |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [**ScheduleByMonthDayOfWeek**](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) | [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) | 指定啟動工作的觸發程式，此觸發程式會每個月的每週工作日排程。<br/> |



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

針對開發腳本，使用 [**MonthlyDOWTrigger. DaysOfWeek**](monthlydowtrigger-daysofweek.md) 屬性指定每週每月星期幾行事曆的天數。

若是 c + + 開發，則會使用 [**IMonthlyDOWTrigger：:D aysofweek**](/windows/desktop/api/taskschd/nf-taskschd-imonthlydowtrigger-get_daysofweek) 屬性指定每週每週的日曆日。

上述的子項目是由 [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) 複雜型別定義。

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
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[工作排程器架構元素](task-scheduler-schema-elements.md)
</dt> <dt>

[工作排程器](task-scheduler-start-page.md)
</dt> </dl>

 

 





