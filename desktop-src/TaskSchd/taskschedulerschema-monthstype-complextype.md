---
title: monthsType 複雜類型
description: 定義專案的子專案和排序資訊 (monthlyDayOfWeekScheduleType) 和月份 (monthlyScheduleType) 元素。
ms.assetid: f1faa67a-2f5f-4a00-a1df-2d44e218278b
keywords:
- monthsType 複雜類型工作排程器
topic_type:
- apiref
api_name:
- monthsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a0873f07cc76af9fab827c3df98a8f08ef300de93d4ae6b316809ba32aac87ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117758744"
---
# <a name="monthstype-complex-type"></a>monthsType 複雜類型

定義專案的子專案和排序資訊 [**(monthlyDayOfWeekScheduleType)**](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) 和 [**月份 (monthlyScheduleType)**](taskschedulerschema-months-monthlyscheduletype-element.md) 元素。

``` syntax
<xs:complexType name="monthsType">
    <xs:all>
        <xs:element name="January"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="February"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="March"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="April"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="May"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="June"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="July"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="August"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="September"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="October"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="November"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="December"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a>子元素



| 元素                                                               | 類型 | 描述                                            |
|-----------------------------------------------------------------------|------|--------------------------------------------------------|
| [**四月**](taskschedulerschema-april-monthstype-element.md)         | N/A  | 指定工作會在四月執行。 <br/>     |
| [**8 月**](taskschedulerschema-august-monthstype-element.md)       | N/A  | 指定工作在8月執行。 <br/>    |
| [**十二月**](taskschedulerschema-december-monthstype-element.md)   | N/A  | 指定工作會在十二月執行。 <br/>  |
| [**2 月**](taskschedulerschema-february-monthstype-element.md)   | N/A  | 指定工作會在二月執行。 <br/>  |
| [**一月**](taskschedulerschema-january-monthstype-element.md)     | N/A  | 指定工作會在一月執行。 <br/>   |
| [**7 月**](taskschedulerschema-july-monthstype-element.md)           | N/A  | 指定工作會在七月執行。 <br/>      |
| [**6 月**](taskschedulerschema-june-monthstype-element.md)           | N/A  | 指定工作在六月執行。 <br/>      |
| [**3 月**](taskschedulerschema-march-monthstype-element.md)         | N/A  | 指定工作在三月執行。 <br/>     |
| [**可能**](taskschedulerschema-may-monthstype-element.md)             | N/A  | 指定工作在5月執行。 <br/>       |
| [**十一月**](taskschedulerschema-november-monthstype-element.md)   | N/A  | 指定工作在11月執行。 <br/>  |
| [**10 月**](taskschedulerschema-october-monthstype-element.md)     | N/A  | 指定工作在十月執行。 <br/>   |
| [**9 月**](taskschedulerschema-september-monthstype-element.md) | N/A  | 指定工作在九月執行。 <br/> |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[工作排程器架構複雜類型](task-scheduler-schema-complex-types.md)
</dt> <dt>

[工作排程器](task-scheduler-start-page.md)
</dt> </dl>

 

 





