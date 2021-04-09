---
title: 間隔 (restartType) 元素
description: 指定工作排程器將嘗試重新開機工作的時間長度。
ms.assetid: 00b8fcbb-5be8-4bf1-92a0-2afd2a50f8e1
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
ms.openlocfilehash: c97e754e0b29a43d6ba419bd806404fe1b85b2b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934015"
---
# <a name="interval-restarttype-element"></a>間隔 (restartType) 元素

指定工作排程器將嘗試重新開機工作的時間長度。 此字串的格式為 P <days> DT <hours> H <minutes> M <seconds> S (例如，"PT5M" 為5分鐘、"PT1H" 為1小時，而 "PT20M" 為20分鐘) 。 允許的時間上限為31天，而允許的最短時間為1分鐘。

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

元素是由 [**restartType**](taskschedulerschema-restarttype-complextype.md) 複雜型別定義。

## <a name="parent-element"></a>父元素



| 元素                                                                               | 衍生自                                                       | Description                                                                                                     |
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [**RestartOnFailure**](taskschedulerschema-restartonfailure-settingstype-element.md) | [**restartType**](taskschedulerschema-restarttype-complextype.md) | 指定當工作因為任何原因而失敗時，工作排程器將嘗試重新開機工作。<br/> |



## <a name="remarks"></a>備註

如果指定這個元素，則也必須指定 [**Count**](taskschedulerschema-count-restarttype-element.md) 元素，以告知工作排程器應該嘗試重新開機工作的次數。

針對 c + + 開發，請參閱 [**ITaskSettings 的 RestartInterval 屬性**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_restartinterval)。

如需腳本開發，請參閱 [**TaskSettings. RestartInterval**](tasksettings-restartinterval.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[工作排程器架構元素](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





