---
title: idleSettingsType 複雜類型
description: 定義 IdleSettings (settingsType) 元素的子項目和排序資訊。
ms.assetid: 0f50c4d6-fda9-42cc-8dab-4c9439fbea4b
keywords:
- idleSettingsType 複雜類型工作排程器
topic_type:
- apiref
api_name:
- idleSettingsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ba5ffa3acb879aad095b5b136d882bb817eb0ab0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967326"
---
# <a name="idlesettingstype-complex-type"></a>idleSettingsType 複雜類型

定義 [**IdleSettings (settingsType)**](taskschedulerschema-idlesettings-settingstype-element.md) 元素的子項目和排序資訊。

``` syntax
<xs:complexType name="idleSettingsType">
    <xs:all>
        <xs:element name="Duration"
            default="PT10M"
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
        <xs:element name="WaitTimeout"
            default="PT1H"
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
        <xs:element name="StopOnIdleEnd"
            type="boolean"
            default="true"
            minOccurs="0"
         />
        <xs:element name="RestartOnIdle"
            type="boolean"
            default="false"
            minOccurs="0"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a>子元素



| 元素                                                                                  | 類型    | Description                                                                                                                                                                                                       |
|------------------------------------------------------------------------------------------|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**持續時間**](taskschedulerschema-duration-idlesettingstype-element.md)                |         | 指定在閒置條件下，允許啟動工作的時間量。<br/>                                                                                                                     |
| [**RestartOnIdle**](taskschedulerschema-restartonidle-idlesettingstype-element.md)      | boolean | 當閒置條件啟動時，就會立即重新開機工作。<br/>                                                                                                                                             |
| [**StopOnIdleEnd**](taskschedulerschema-terminateonidleend-idlesettingstype-element.md) | boolean | 指定如果閒置條件在超過閒置持續時間之前結束，則工作會終止。<br/>                                                                                                 |
| [**WaitTimeout**](taskschedulerschema-waittimeout-idlesettingstype-element.md)          |         | 指定等待閒置條件啟動的時間量。 如果未指定這個專案的值，工作排程器服務將會無限期地等候閒置的情況發生。<br/> |



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

 

 





