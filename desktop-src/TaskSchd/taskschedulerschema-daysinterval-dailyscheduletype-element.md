---
title: DaysInterval (dailyScheduleType) 元素
description: 指定排程中天數之間的間隔。
ms.assetid: 495ea1c0-37eb-4b12-8241-bfc6489e33ed
keywords:
- DaysInterval 元素工作排程器
topic_type:
- apiref
api_name:
- DaysInterval
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 97b50581aa4825b31983a234a5eb47ff7b7b7e06
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934019"
---
# <a name="daysinterval-dailyscheduletype-element"></a>DaysInterval (dailyScheduleType) 元素

指定排程中天數之間的間隔。

``` syntax
<xs:element name="DaysInterval"
    minOccurs="0"
>
    <xs:simpleType>
        <xs:restriction
            base="unsignedInt"
        >
            <xs:minInclusive
                value="1"
             />
            <xs:maxInclusive
                value="365"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

元素是由 [**dailyScheduleType**](taskschedulerschema-dailyscheduletype-complextype.md) 複雜型別定義。

## <a name="parent-element"></a>父元素



| 元素                                                                                | 衍生自                                                                   | Description                            |
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|----------------------------------------|
| [**ScheduleByDay**](taskschedulerschema-schedulebyday-calendartriggertype-element.md) | [**dailyScheduleType**](taskschedulerschema-dailyscheduletype-complextype.md) | 指定每日排程。<br/> |



## <a name="remarks"></a>備註

針對腳本開發，每日觸發程式的天數間隔是由 [**DailyTrigger. DaysInterval**](dailytrigger-daysinterval.md) 屬性所指定。

針對 c + + 開發，每日觸發程式的天數間隔是由 [**IDailyTrigger：:D aysinterval**](/windows/desktop/api/taskschd/nf-taskschd-idailytrigger-get_daysinterval) 屬性所指定。

## <a name="examples"></a>範例

下列 XML 會定義每日啟動工作的每日行事曆觸發程式。


```XML
<CalendarTrigger>
    <StartBoundary>2005-01-01T00:00:00</StartBoundary>
    <EndBounadry>2007-01-01T00:00:00</EndBoundary>
    <ScheduleByDay>
        <DaysInterval>1</DaysInterval>
    </ScheduleByDay>
</CalendarTrigger>
```



如需指定每日排程之工作的 XML 完整範例，請參閱 [ (XML) 的每日觸發程式範例 ](daily-trigger-example--xml-.md)。

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

 

 





