---
title: 星期六 (daysOfWeekType) 元素
description: 指定工作在星期六執行。
ms.assetid: def26a72-c143-466a-b5b0-6105078afffa
keywords:
- 星期六元素工作排程器
topic_type:
- apiref
api_name:
- Saturday
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0592d4f5f005afa1136d06261b05d4d4a942ac490140d384bb9174555b49c253
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099898"
---
# <a name="saturday-daysofweektype-element"></a>星期六 (daysOfWeekType) 元素

指定工作在星期六執行。

``` syntax
<xs:element name="Saturday">
    <xs:complexType />
</xs:element>
```

**星期六** 元素是由 [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md)複雜型別定義。

## <a name="parent-element"></a>父元素



| 元素                                                                                                                  | 衍生自                                                             | 描述                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [**DaysOfWeek (monthlyDayOfWeekScheduleType)**](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) | [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) | 指定工作在一周中的哪幾天執行一周的每月日排程。<br/> |
| [**DaysOfWeek (weeklyScheduleType)**](taskschedulerschema-daysofweek-weeklyscheduletype-element.md)                     | [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) | 指定每週排程執行工作的天數。<br/>              |



## <a name="examples"></a>範例

下列 XML 會定義在星期六開始工作的星期幾行事曆。


```XML
<DaysOfWeek>
    <Saturday/>
</DaysOfWeek>
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

 

 





