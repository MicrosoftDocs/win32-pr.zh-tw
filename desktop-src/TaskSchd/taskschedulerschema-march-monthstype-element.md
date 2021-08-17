---
title: 三月 (monthsType) 元素
description: 指定工作在三月執行。
ms.assetid: 0cd82405-8e17-483d-88ba-32cae590f6b3
keywords:
- 三月元素工作排程器
topic_type:
- apiref
api_name:
- March
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8d90d64e0fd275f57252cd435ae5dc42abfe8ba17613e1b20425fc27c515509e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139181"
---
# <a name="march-monthstype-element"></a>三月 (monthsType) 元素

指定工作在三月執行。

``` syntax
<xs:element name="March">
    <xs:complexType />
</xs:element>
```

**三月份** 元素是由 [**monthsType**](taskschedulerschema-monthstype-complextype.md)複雜型別定義。

## <a name="parent-element"></a>父元素



| 元素                                                                                                          | 衍生自                                                     | 描述                                                                                                |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**MonthlyDayOfWeekScheduleType) 的月份 (**](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) | [**monthsType**](taskschedulerschema-monthstype-complextype.md) | 指定在一年中的幾個月，工作會在一年中執行一周的每月日排程。<br/> |
| [**MonthlyScheduleType) 的月份 (**](taskschedulerschema-months-monthlyscheduletype-element.md)                   | [**monthsType**](taskschedulerschema-monthstype-complextype.md) | 指定執行每月排程之工作的年度月份。<br/>             |



## <a name="examples"></a>範例

下列 XML 定義在三月執行工作的月份行事曆。


```XML
<Months>
    <March/>
</Months>
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

 

 





