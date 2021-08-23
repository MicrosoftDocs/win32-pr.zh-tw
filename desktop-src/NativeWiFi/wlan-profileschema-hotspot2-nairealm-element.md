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
ms.openlocfilehash: 084ee3ce04a560ce50c3ab0391f808bc09aed1bb90da6a34b86755b9b64ae772
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119684208"
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



 

 



