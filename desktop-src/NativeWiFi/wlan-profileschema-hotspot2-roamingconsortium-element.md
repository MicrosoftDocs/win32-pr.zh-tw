---
description: 由 IEEE 指派 (OUI) 的組織唯一識別碼清單。
ms.assetid: 4a9885b6-2e57-4a16-8e1d-b5b0797e09db
title: RoamingConsortium (Hotspot2) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RoamingConsortium
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 5e53fa274cbc56de6be026ef0e466ec501cf9124
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971685"
---
# <a name="roamingconsortium-hotspot2-element"></a>RoamingConsortium (Hotspot2) 元素

由 IEEE 指派 (OUI) 的組織唯一識別碼清單。

``` syntax
<xs:element name="RoamingConsortium"
    minOccurs="0"
>
    <xs:complexType>
        <xs:sequence>
            <xs:element name="OUI"
                minOccurs="0"
                maxOccurs="256"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="hexBinary"
                    >
                        <xs:minLength
                            value="3"
                         />
                        <xs:maxLength
                            value="5"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

元素是由 [**Hotspot2**](wlan-profileschema-hotspot2-element.md) 元素所定義。

## <a name="child-elements"></a>子元素



| 元素 | 類型 | Description                                                               |
|---------|------|---------------------------------------------------------------------------|
| OUI     |      | 單一的 OUI，格式為可變大小的十六進位數位。<br/> |



 

 




