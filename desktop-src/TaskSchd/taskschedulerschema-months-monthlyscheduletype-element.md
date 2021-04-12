---
title: MonthlyScheduleType) 元素 (月份
description: 指定執行每月排程之工作的年度月份。
ms.assetid: 71c9f7ac-01fc-4837-bccf-1869df2bc24e
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
ms.openlocfilehash: 0ed40fd2466f8962f839f39e7addd3b7e1bc33eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105371"
---
# <a name="months-monthlyscheduletype-element"></a>MonthlyScheduleType) 元素 (月份

指定執行每月排程之工作的年度月份。

``` syntax
<xs:element name="Months"
    type="monthsType"
 />
```

**Months** 元素是由 [**monthlyScheduleType**](taskschedulerschema-monthlyscheduletype-complextype.md)複雜型別定義。

## <a name="parent-element"></a>父元素



| 元素                                                                                    | 衍生自                                                                       | Description                               |
|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|-------------------------------------------|
| [**ScheduleByMonth**](taskschedulerschema-schedulebymonth-calendartriggertype-element.md) | [**monthlyScheduleType**](taskschedulerschema-monthlyscheduletype-complextype.md) | 指定每月排程。 <br/> |



## <a name="child-elements"></a>子元素



| 元素                                                                            | 類型 | Description                                           |
|------------------------------------------------------------------------------------|------|-------------------------------------------------------|
| [**四月 (monthsType)**](taskschedulerschema-april-monthstype-element.md)         |      | 指定工作會在四月執行。<br/>     |
| [**八月 (monthsType)**](taskschedulerschema-august-monthstype-element.md)       |      | 指定工作在8月執行。<br/>    |
| [**12月 (monthsType)**](taskschedulerschema-december-monthstype-element.md)   |      | 指定工作會在十二月執行。<br/>  |
| [**二月 (monthsType)**](taskschedulerschema-february-monthstype-element.md)   |      | 指定工作會在二月執行。<br/>  |
| [**1月 (monthsType)**](taskschedulerschema-january-monthstype-element.md)     |      | 指定工作會在一月執行。<br/>   |
| [**七月 (monthsType)**](taskschedulerschema-july-monthstype-element.md)           |      | 指定工作會在七月執行。<br/>      |
| [**六月 (monthsType)**](taskschedulerschema-june-monthstype-element.md)           |      | 指定工作在六月執行。<br/>      |
| [**三月 (monthsType)**](taskschedulerschema-march-monthstype-element.md)         |      | 指定工作在三月執行。<br/>     |
| [**可能 (monthsType)**](taskschedulerschema-may-monthstype-element.md)             |      | 指定工作在5月執行。<br/>       |
| [**11月 (monthsType)**](taskschedulerschema-november-monthstype-element.md)   |      | 指定工作在11月執行。<br/>  |
| [**十月 (monthsType)**](taskschedulerschema-october-monthstype-element.md)     |      | 指定工作在十月執行。<br/>   |
| [**MonthsType) 的九月 (**](taskschedulerschema-september-monthstype-element.md) |      | 指定工作在九月執行。<br/> |



## <a name="remarks"></a>備註

針對腳本開發，會使用 [**MonthlyTrigger MonthsOfYear**](monthlytrigger-monthsofyear.md) 屬性指定排程的月份。

針對 c + + 開發，會使用 [**IMonthlyTrigger：： MonthsOfYear**](/windows/desktop/api/taskschd/nf-taskschd-imonthlytrigger-get_monthsofyear) 屬性指定排程的月份。

## <a name="examples"></a>範例

下列 XML 會定義每月首次開始工作的月曆，並在每個月的第15天開始。


```XML
</ScheduleByMonth>
    <DaysOfMonth>
        <Day>1</Day>
        <Day>15</Day>
    </DaysOfMonth
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

 

 





