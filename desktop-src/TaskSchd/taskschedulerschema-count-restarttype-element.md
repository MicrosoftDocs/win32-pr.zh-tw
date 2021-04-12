---
title: Count (restartType) 元素
description: 指定工作排程器將嘗試重新開機工作的次數。
ms.assetid: 67466c14-c9dd-49c8-a6ed-df7531fc63b8
keywords:
- Count 元素工作排程器
topic_type:
- apiref
api_name:
- Count
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 655f636b725e48749540d67710afa57b3c45c89c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464809"
---
# <a name="count-restarttype-element"></a>Count (restartType) 元素

指定工作排程器將嘗試重新開機工作的次數。

``` syntax
<xs:element name="Count">
    <xs:simpleType>
        <xs:restriction
            base="unsignedByte"
        >
            <xs:minInclusive
                value="1"
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

如果指定這個元素，則也必須指定 [**Interval**](taskschedulerschema-interval-restarttype-element.md) 元素，以告知工作排程器要嘗試重新開機工作的時間長度。

針對 c + + 開發，請參閱 [**ITaskSettings 的 RestartCount 屬性**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_restartcount)。

如需腳本開發，請參閱 [**TaskSettings. RestartCount**](tasksettings-restartcount.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[工作排程器架構元素](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





