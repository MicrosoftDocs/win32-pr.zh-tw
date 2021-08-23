---
title: 七月 (monthsType) 元素
description: 指定工作會在七月執行。
ms.assetid: 6fcb06f1-0806-469c-a283-ba8f2ba2c256
keywords:
- 七月元素工作排程器
topic_type:
- apiref
api_name:
- July
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3e62ad0f04dcf8ec12d31ddc5ff6372896fd49442689cae7cdc82810b19a9138
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119575218"
---
# <a name="july-monthstype-element"></a>七月 (monthsType) 元素

指定工作會在七月執行。

``` syntax
<xs:element name="July">
    <xs:complexType />
</xs:element>
```

**七月** 元素是由 [**monthsType**](taskschedulerschema-monthstype-complextype.md)複雜型別定義。

## <a name="parent-element"></a>父元素



| 元素                                                                                                          | 衍生自                                                     | 描述                                                                                                |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**MonthlyDayOfWeekScheduleType) 的月份 (**](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) | [**monthsType**](taskschedulerschema-monthstype-complextype.md) | 指定在一年中的幾個月，工作會在一年中執行一周的每月日排程。<br/> |
| [**MonthlyScheduleType) 的月份 (**](taskschedulerschema-months-monthlyscheduletype-element.md)                   | [**monthsType**](taskschedulerschema-monthstype-complextype.md) | 指定執行每月排程之工作的年度月份。<br/>             |



## <a name="examples"></a>範例

下列 XML 會定義月曆，以在7月執行工作。


```XML
<Months>
    <July/>
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

 

 





