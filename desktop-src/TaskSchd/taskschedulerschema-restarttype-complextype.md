---
title: restartType 複雜類型
description: 定義 RestartOnFailure 元素的子項目和順序資訊。
ms.assetid: 3a192955-8a33-42b9-a974-faa9a3789f58
keywords:
- restartType 複雜類型工作排程器
topic_type:
- apiref
api_name:
- restartType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 996debc2c8e3d7d00ca7b42facde582f918d72736426ed326691461d800f8562
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119516477"
---
# <a name="restarttype-complex-type"></a>restartType 複雜類型

定義 [RestartOnFailure](taskschedulerschema-restartonfailure-settingstype-element.md) 元素的子項目和順序資訊。

``` syntax
<xs:complexType name="restartType">
    <xs:all>
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
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a>子元素



| 元素                                                              | 類型 | 描述                                        |
|----------------------------------------------------------------------|------|----------------------------------------------------|
| [**計數**](taskschedulerschema-count-restarttype-element.md)       |      | 重新開機工作的嘗試次數。<br/> |
| [**間隔**](taskschedulerschema-interval-restarttype-element.md) |      | 嘗試啟動工作的時間長度。<br/>      |



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

 

 





