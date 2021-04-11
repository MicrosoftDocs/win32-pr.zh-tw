---
title: 持續時間 (repetitionType) 元素
description: 指定重複模式的時間長度。
ms.assetid: a24f3827-18b2-465e-b132-77dce139e0d4
keywords:
- Duration 元素工作排程器
topic_type:
- apiref
api_name:
- Duration
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3772abb0224b03db4985de126e1d9cc0058ab5de
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317507"
---
# <a name="duration-repetitiontype-element"></a>持續時間 (repetitionType) 元素

指定重複模式的時間長度。 此字串的格式為 PnYnMnDTnHnMnS，其中 nY 是年數，nM 是月數，nD 是天數、t ' 是日期/時間分隔符號、nH 是時數、nM 為分鐘數，而 nS 是以秒為單位的秒數，例如，PT5M 指定 (5 分鐘，P1M4DT2H5M 指定一個月、四天、兩小時和五分鐘的) 。 如需持續時間類型的詳細資訊，請參閱 <https://go.microsoft.com/fwlink/p/?linkid=106886> 。 如果未在持續時間內指定任何值，則會無限期地重複模式。 最小值是一分鐘。

``` syntax
<xs:element name="Duration"
    minOccurs="0"
>
    <xs:simpleType>
        <xs:restriction
            base="duration"
        >
            <xs:minInclusive
                value="PT1M"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

元素是由 [**repetitionType**](taskschedulerschema-repetitiontype-complextype.md) 複雜型別定義。

## <a name="parent-element"></a>父元素



| 元素                                                                      | 衍生自                                                             | Description                                                                                                               |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [**重複**](taskschedulerschema-repetition-triggerbasetype-element.md) | [**repetitionType**](taskschedulerschema-repetitiontype-complextype.md) | 指定執行工作的頻率，以及啟動工作之後重複模式重複的時間長度。<br/> |



## <a name="remarks"></a>備註

若為腳本應用程式，則會使用 [**RepetitionPattern duration**](repetitionpattern-duration.md) 屬性指定模式的持續時間。

若是 c + + 應用程式，則會使用 [**IRepetitionPattern：:D uration**](/windows/desktop/api/taskschd/nf-taskschd-irepetitionpattern-get_duration) 屬性指定模式的持續時間。

## <a name="examples"></a>範例

下列 XML 會定義觸發程式的重複模式。


```XML
<Repetition>
    <Interval></Interval>
    <Duration></Duration>
    <StopAtDurationEnd>true</StopAtDirationEnd>
</Repetition>
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

 

 





