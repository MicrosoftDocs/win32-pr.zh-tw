---
title: maintenanceSettingsType 複雜類型
description: 定義 MaintenanceSettings 元素的子項目和排序資訊。
ms.assetid: CA4C452E-CA25-4E2D-B5E2-ED64C59AB3AD
keywords:
- maintenanceSettingsType 複雜類型工作排程器
topic_type:
- apiref
api_name:
- maintenanceSettingsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f0733d16ec929b4e67774fc436c1530b67d70392b2655525b2aaaa642c2ea346
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139201"
---
# <a name="maintenancesettingstype-complex-type"></a>maintenanceSettingsType 複雜類型

定義 [**MaintenanceSettings**](taskschedulerschema-maintenancesettings-maintenancesettingstype-element.md) 元素的子項目和排序資訊。

``` syntax
<xs:complexType name="maintenanceSettingsType">
    <xs:all>
        <xs:element name="Period"
            minOccurs="1"
            maxOccurs="1"
        >
            <xs:simpleType>
                <xs:restriction
                    base="duration"
                >
                    <xs:minInclusive
                        value="P1D"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
        <xs:element name="Deadline"
            minOccurs="1"
            maxOccurs="1"
        >
            <xs:simpleType>
                <xs:restriction
                    base="duration"
                >
                    <xs:minInclusive
                        value="P1D"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
        <xs:element name="Exclusive"
            type="boolean"
            maxOccurs="1"
            minOccurs="1"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a>子元素



| 元素                                                                        | 類型    | 描述                                                                                                                                                                                    |
|--------------------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**期限**](taskschedulerschema-daysinterval-dailyscheduletype-element.md) |         | 指定當工作排程器在正常維護期間無法完成時，在緊急自動維護期間，工作排程器將嘗試啟動工作的時間量。<br/> |
| **排除**                                                                  | boolean | 如果設定為 true，則工作將會在其他維護工作中以獨佔方式啟動。<br/>                                                                                                 |
| [**期間**](taskschedulerschema-daysinterval-dailyscheduletype-element.md)   |         | 指定在自動維護期間必須啟動工作的頻率。<br/>                                                                                                      |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[僅限桌面應用程式\]<br/>           |
| 最低支援的伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[工作排程器架構複雜類型](task-scheduler-schema-complex-types.md)
</dt> <dt>

[工作排程器](task-scheduler-start-page.md)
</dt> </dl>

 

 





