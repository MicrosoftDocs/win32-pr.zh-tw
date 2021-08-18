---
title: 間隔 (repetitionType) 元素
description: 指定工作每次重新開機之間的時間量。
ms.assetid: 28c6475a-88e3-44ac-92c7-6f463e8460c9
keywords:
- Interval 元素工作排程器
topic_type:
- apiref
api_name:
- Interval
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ec6f2724f4374ed94fff47e6577a2887ca953cae0af66de9c64971cd80aa2050
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099998"
---
# <a name="interval-repetitiontype-element"></a>間隔 (repetitionType) 元素

指定工作每次重新開機之間的時間量。 此字串的格式為 `P<days>DT<hours>H<minutes>M<seconds>S` (例如，"PT5M" 為5分鐘、"PT1H" 為1小時，而 "PT20M" 為20分鐘) 。 允許的時間上限為31天，而允許的最短時間為1分鐘。

``` syntax
<xs:element name="Interval">
    <xs:simpleType>
        <xs:restriction
            base="duration"
        >
            <xs:minInclusive
                value="PT1M"
             />
            <xs:maxInclusive
                value="P31D"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

元素是由 [**repetitionType**](taskschedulerschema-repetitiontype-complextype.md) 複雜型別定義。

## <a name="parent-element"></a>父元素



| 元素                                                                      | 衍生自                                                             | 描述                                                                                                               |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [**重複**](taskschedulerschema-repetition-triggerbasetype-element.md) | [**repetitionType**](taskschedulerschema-repetitiontype-complextype.md) | 指定執行工作的頻率，以及啟動工作之後重複模式重複的時間長度。<br/> |



## <a name="remarks"></a>備註

針對腳本開發，重複模式的間隔是使用 [**RepetitionPattern. interval**](repetitionpattern-interval.md) 屬性來指定。

針對 c + + 開發，會使用 [**IRepetitionPattern：： interval**](/windows/desktop/api/taskschd/nf-taskschd-irepetitionpattern-get_interval) 屬性指定重複模式的間隔。

## <a name="examples"></a>範例

如需使用重複間隔之工作的 XML 完整範例，請參閱 [ (xml) 的每日觸發程式範例 ](daily-trigger-example--xml-.md)。

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

 

 





