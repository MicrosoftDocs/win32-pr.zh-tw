---
title: 星期日 (daysOfWeekType) 元素
description: 指定工作在星期日執行。
ms.assetid: 856db869-2273-4bb8-88c8-c126bb16c87b
keywords:
- 星期日元素工作排程器
topic_type:
- apiref
api_name:
- Sunday
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 40efba31b392da5959853feeb1cae567cee25cc7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105353"
---
# <a name="sunday-daysofweektype-element"></a>星期日 (daysOfWeekType) 元素

指定工作在星期日執行。

``` syntax
<xs:element name="Sunday">
    <xs:complexType />
</xs:element>
```

**星期日** 元素是由 [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md)複雜型別定義。

## <a name="parent-element"></a>父元素



| 元素                                                                                                                  | 衍生自                                                             | Description                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [**DaysOfWeek (monthlyDayOfWeekScheduleType)**](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) | [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) | 指定工作在一周中的哪幾天執行一周的每月日排程。<br/> |
| [**DaysOfWeek (weeklyScheduleType)**](taskschedulerschema-daysofweek-weeklyscheduletype-element.md)                     | [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) | 指定每週排程執行工作的天數。<br/>              |



## <a name="examples"></a>範例

下列 XML 會定義在星期日啟動工作的星期幾行事曆。


```XML
<DaysOfWeek>
    <Sunday/>
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

 

 





