---
description: " (NAI) 領域識別碼的網路存取識別碼清單。"
ms.assetid: e77802ee-4017-4f04-ae71-5d6d0de8fcf3
title: NAIRealm (Hotspot2) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NAIRealm
api_type:
- Schema
api_location: ''
ms.openlocfilehash: a7c8fcf85bd23c13f0e7501d59c3db62c2bf82f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512521"
---
# <a name="nairealm-hotspot2-element"></a>NAIRealm (Hotspot2) 元素

 (NAI) 領域識別碼的網路存取識別碼清單。 這份清單中的專案通常是表單 `user@domain` 。 [NAI 領域] 清單是識別大部分非行動運算子（例如 Mso、有線操作員和公用場地）的慣用方法。

``` syntax
<xs:element name="NAIRealm"
    minOccurs="0"
>
    <xs:complexType>
        <xs:sequence>
            <xs:element name="name"
                maxOccurs="256"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="string"
                    >
                        <xs:minLength
                            value="1"
                         />
                        <xs:maxLength
                            value="255"
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



| 元素 | 類型 | 描述                                                   |
|---------|------|---------------------------------------------------------------|
| NAME    |      | 單一領域識別碼。 通常是表單 `user@domain` 。 |



 

 



