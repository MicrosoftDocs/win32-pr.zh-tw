---
title: DaysOfMonth (monthlyScheduleType) 元素
description: 指定工作執行的當月天數。
ms.assetid: 62f28f44-b3d8-414e-80d4-f4d8bd3c4527
keywords:
- DaysOfMonth 元素工作排程器
topic_type:
- apiref
api_name:
- DaysOfMonth
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 38c2106f8d612ee27dc1297023a59b531fa9548d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965120"
---
# <a name="daysofmonth-monthlyscheduletype-element"></a>DaysOfMonth (monthlyScheduleType) 元素

指定工作執行的當月天數。

``` syntax
<xs:element name="DaysOfMonth"
    type="daysOfMonthType"
 />
```

**DaysOfMonth** 元素是由 [**monthlyScheduleType**](taskschedulerschema-monthlyscheduletype-complextype.md)複雜型別定義。

## <a name="parent-element"></a>父元素



| 元素                                                                                    | 衍生自                                                                                         | Description                                                                          |
|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [**ScheduleByMonth**](taskschedulerschema-schedulebymonth-calendartriggertype-element.md) | [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) | 指定啟動工作的觸發程式，此觸發程式會每個月的每週工作日排程。<br/> |



## <a name="child-elements"></a>子元素



| 元素                                                        | 類型                                                                    | Description                                                         |
|----------------------------------------------------------------|-------------------------------------------------------------------------|---------------------------------------------------------------------|
| [**天**](taskschedulerschema-day-daysofmonthtype-element.md) | [**dayOfMonthType**](taskschedulerschema-dayofmonthtype-simpletype.md) | 指定執行工作的月份日期。<br/> |



## <a name="remarks"></a>備註

針對腳本開發，系統會使用 [**MonthlyTrigger. DaysOfMonth**](monthlytrigger-daysofmonth.md) 屬性指定該排程的當月天數。

針對 c + + 開發，會使用 [**IMonthlyTrigger：:D aysofmonth**](/windows/desktop/api/taskschd/nf-taskschd-imonthlytrigger-get_daysofmonth) 屬性來指定排程的當月天數。

工作要執行的每個月的每一天都必須重複子項目。

## <a name="examples"></a>範例

下列 XML 會定義每月的行事曆觸發程式，此觸發程式會在每個月的第一天) 的上午8:30 開始工作 (。


```XML
<CalendarTrigger>
    <StartBoundary>2005-01-01T08:00:00</StartBoundary>
    <EndBounadry>2007-01-01T00:00:00</EndBoundary>
    <ScheduleByMonth>
        <DaysOfMonth>
            <Day>1</Day>  
        </DaysOfMonth>
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
    </ScheduleByMonth>
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

 

 





