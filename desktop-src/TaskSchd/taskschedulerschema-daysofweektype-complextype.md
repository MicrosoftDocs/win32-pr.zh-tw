---
title: daysOfWeekType 複雜類型
description: 定義 DaysOfWeek (weeklyScheduleType) 和 DaysOfWeek (monthlyDayOfWeekScheduleType) 元素的子項目和排序資訊。
ms.assetid: b3315582-af7a-4d4c-8f6f-61de12a85f46
keywords:
- daysOfWeekType 複雜類型工作排程器
topic_type:
- apiref
api_name:
- daysOfWeekType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0b4a1b5e6aeaa77c0bdfe12b1d5b68fde018f236
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317511"
---
# <a name="daysofweektype-complex-type"></a>daysOfWeekType 複雜類型

定義 [**DaysOfWeek (weeklyScheduleType)**](taskschedulerschema-daysofweek-weeklyscheduletype-element.md) 和 [**DaysOfWeek (monthlyDayOfWeekScheduleType)**](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) 元素的子項目和排序資訊。

``` syntax
<xs:complexType name="daysOfWeekType">
    <xs:all>
        <xs:element name="Monday"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="Tuesday"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="Wednesday"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="Thursday"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="Friday"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="Saturday"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="Sunday"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a>子元素



| 元素                                                                   | 類型 | Description                         |
|---------------------------------------------------------------------------|------|-------------------------------------|
| [**星期五**](taskschedulerschema-friday-daysofweektype-element.md)       | N/A  | 工作會在星期五執行。 <br/>    |
| [**星期一**](taskschedulerschema-monday-daysofweektype-element.md)       | N/A  | 工作會在星期一執行。<br/>     |
| [**星期六**](taskschedulerschema-saturday-daysofweektype-element.md)   | N/A  | 工作會在星期六執行。 <br/>  |
| [**星期日**](taskschedulerschema-sunday-daysofweektype-element.md)       | N/A  | 工作會在星期日執行。 <br/>    |
| [**Thursday**](taskschedulerschema-thursday-daysofweektype-element.md)   | N/A  | 工作在星期四執行 <br/>   |
| [**Tuesday**](taskschedulerschema-tuesday-daysofweektype-element.md)     | N/A  | 工作會在星期二執行。 <br/>   |
| [**星期三**](taskschedulerschema-wednesday-daysofweektype-element.md) | N/A  | 工作會在星期三執行。 <br/> |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[工作排程器架構複雜類型](task-scheduler-schema-complex-types.md)
</dt> <dt>

[工作排程器](task-scheduler-start-page.md)
</dt> </dl>

 

 





