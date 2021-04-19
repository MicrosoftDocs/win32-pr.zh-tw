---
title: 11月 (monthsType) 元素
description: 指定工作在11月執行。
ms.assetid: 45f8c47b-3884-4f18-8275-f29f82ee32e2
keywords:
- 十一月元素工作排程器
topic_type:
- apiref
api_name:
- November
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 295b63a4ff4dad1ec07504bb43c4a471d4389159
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966323"
---
# <a name="november-monthstype-element"></a>11月 (monthsType) 元素

指定工作在11月執行。

``` syntax
<xs:element name="November">
    <xs:complexType />
</xs:element>
```

**11 月** 的元素是由 [**monthsType**](taskschedulerschema-monthstype-complextype.md)複雜型別定義。

## <a name="parent-element"></a>父元素



| 元素                                                                                                          | 衍生自                                                     | Description                                                                                                |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**MonthlyDayOfWeekScheduleType) 的月份 (**](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) | [**monthsType**](taskschedulerschema-monthstype-complextype.md) | 指定在一年中的幾個月，工作會在一年中執行一周的每月日排程。<br/> |
| [**MonthlyScheduleType) 的月份 (**](taskschedulerschema-months-monthlyscheduletype-element.md)                   | [**monthsType**](taskschedulerschema-monthstype-complextype.md) | 指定執行每月排程之工作的年度月份。<br/>             |



## <a name="examples"></a>範例

下列 XML 會定義在11月執行工作的月份行事曆。


```XML
<Months>
    <November/>
</DaysOfWeek>
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

 

 





